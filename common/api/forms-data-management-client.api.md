## API Report File for "@bentley/forms-data-management-client"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { AuthorizedClientRequestContext } from '@bentley/itwin-client';
import { WsgClient } from '@bentley/itwin-client';
import { WsgInstance } from '@bentley/itwin-client';

// @internal (undocumented)
export class Attachment extends WsgInstance {
    // (undocumented)
    binding?: string;
    // (undocumented)
    createdDate?: string;
    // (undocumented)
    modifiedDate?: string;
    // (undocumented)
    name?: string;
    // (undocumented)
    sasUrl?: string;
    // (undocumented)
    size?: number;
    // (undocumented)
    type?: string;
}

// @internal (undocumented)
export class AuditRecord extends WsgInstance {
    // (undocumented)
    action?: string;
    // (undocumented)
    recordBy?: string;
    // (undocumented)
    recordById?: string;
    // (undocumented)
    recordDate?: string;
    // (undocumented)
    text?: string;
    // (undocumented)
    values?: AuditValue[];
}

// @internal (undocumented)
export class Comment extends WsgInstance {
    // (undocumented)
    author?: string;
    // (undocumented)
    authorId?: string;
    // (undocumented)
    createdDate?: string;
    // (undocumented)
    fromStateId?: string;
    // (undocumented)
    fromStateName?: string;
    // (undocumented)
    isWorkflowNote?: boolean;
    // (undocumented)
    modifiedDate?: string;
    // (undocumented)
    text?: string;
    // (undocumented)
    toStateId?: string;
    // (undocumented)
    toStateName?: string;
}

// @internal (undocumented)
export class FormDataManagementClient extends WsgClient {
    constructor();
    // (undocumented)
    addNewAttachment(requestContext: AuthorizedClientRequestContext, projectId: string, formClass: string, id: string, attachmentData: string, fileName: string, caption?: string): Promise<string>;
    // (undocumented)
    addWorkflow(requestContext: AuthorizedClientRequestContext, projectId: string, workflow: WorkflowDefinition): Promise<WorkflowDefinition>;
    static buildFormDataFilter(filters: Array<{
        name: string;
        value: string;
    }>): string;
    // (undocumented)
    static readonly configRelyingPartyUri = "imjs_form_data_management_relying_party_uri";
    // (undocumented)
    deleteAttachment(requestContext: AuthorizedClientRequestContext, projectId: string, formClass: string, formId: string, attachmentId: string): Promise<any>;
    // (undocumented)
    deleteWorkflow(requestContext: AuthorizedClientRequestContext, projectId: string, workflowDefId: string): Promise<void>;
    // (undocumented)
    getAttachment(requestContext: AuthorizedClientRequestContext, projectId: string, attachmentId: string): Promise<Attachment[]>;
    // (undocumented)
    getAttachments(requestContext: AuthorizedClientRequestContext, projectId: string, formClass: string, formId: string): Promise<Attachment[]>;
    // (undocumented)
    getAttachmentSasUrl(requestContext: AuthorizedClientRequestContext, projectId: string, attachmentId: string): Promise<Attachment[]>;
    // (undocumented)
    getAuditTrail(requestContext: AuthorizedClientRequestContext, projectId: string, formClass: string, formId: string): Promise<AuditRecord[]>;
    // (undocumented)
    getComments(requestContext: AuthorizedClientRequestContext, projectId: string, formClass: string, formId: string): Promise<Comment[]>;
    getCount(requestContext: AuthorizedClientRequestContext, projectId: string, className: string, filter?: string | FormFilterArray): Promise<InstanceCount[]>;
    getFormData(requestContext: AuthorizedClientRequestContext, projectId: string, className: string, skip?: number, top?: number, filter?: string | Array<{
        name: string;
        value: string;
    }>): Promise<WsgInstance[]>;
    getFormDefinitions(requestContext: AuthorizedClientRequestContext, projectId: string, filter?: string | Array<{
        name: string;
        value: string;
    }>, format?: "json" | "xml"): Promise<FormDefinition[]>;
    // (undocumented)
    getFormInstance(requestContext: AuthorizedClientRequestContext, projectId: string, className: string, instanceId: string): Promise<WsgInstance[]>;
    // (undocumented)
    getFormProperties(requestContext: AuthorizedClientRequestContext, projectId: string, className: string): Promise<any>;
    getIssues(requestContext: AuthorizedClientRequestContext, projectId: string, iModelId?: string): Promise<WsgInstance[]>;
    // (undocumented)
    getProjectMembers(requestContext: AuthorizedClientRequestContext, projectId: string): Promise<ProjectMember[]>;
    // (undocumented)
    getProjectStats(requestContext: AuthorizedClientRequestContext, projectId: string, filter?: string | FormFilterArray): Promise<ProjectStats[]>;
    protected getRelyingPartyUrl(): string;
    protected getUrlSearchKey(): string;
    // (undocumented)
    getWorkflow(requestContext: AuthorizedClientRequestContext, projectId: string, classification: string, discipline: string): Promise<WorkflowDefinition[]>;
    // (undocumented)
    importTemplate(requestContext: AuthorizedClientRequestContext, projectId: string, templateName?: string): Promise<any>;
    // (undocumented)
    postComment(requestContext: AuthorizedClientRequestContext, projectId: string, formClass: string, formId: string, comment: string): Promise<WsgInstance[]>;
    postFormData(requestContext: AuthorizedClientRequestContext, formData: FormInstanceData, projectId: string, className: string, instanceId?: string, formDefId?: string): Promise<WsgInstance>;
    // (undocumented)
    postNewAttachment(requestContext: AuthorizedClientRequestContext, projectId: string, attachmentInstance: object): Promise<any>;
    // (undocumented)
    static readonly searchKey: string;
}

// @internal (undocumented)
export class FormDefinition extends WsgInstance {
    // (undocumented)
    classDisplayLabel?: string;
    // (undocumented)
    classification?: string;
    // (undocumented)
    className?: string;
    // (undocumented)
    classSchema?: string;
    // (undocumented)
    definition?: string;
    // (undocumented)
    discipline?: string;
    // (undocumented)
    errorStatus?: string;
    // (undocumented)
    formId?: string;
    // (undocumented)
    isShared?: boolean;
    // (undocumented)
    name?: string;
    // (undocumented)
    projectId?: string;
    // (undocumented)
    projectName?: string;
    // (undocumented)
    projectNumber?: string;
    // (undocumented)
    shareType?: number;
    // (undocumented)
    status?: string;
    // (undocumented)
    type?: string;
}

// @internal (undocumented)
export type FormFilterArray = Array<{
    name: string;
    value: any;
}>;

// @internal (undocumented)
export class FormInstanceData extends WsgInstance {
    // (undocumented)
    formData?: any;
    // (undocumented)
    properties?: any;
}

// @internal (undocumented)
export class FormProperties extends WsgInstance {
    // (undocumented)
    dateTimeComponent?: string;
    // (undocumented)
    dateTimeKind?: string;
    // (undocumented)
    descriptions?: string;
    // (undocumented)
    displayLabel?: string;
    // (undocumented)
    hidden?: boolean;
    // (undocumented)
    isArray?: boolean;
    // (undocumented)
    isTransient?: boolean;
    // (undocumented)
    name?: string;
    // (undocumented)
    objectDate?: string;
    // (undocumented)
    objectId?: string;
    // (undocumented)
    objectName?: string;
    // (undocumented)
    originClass?: string;
    // (undocumented)
    originClassName?: string;
    // (undocumented)
    overrides?: boolean;
    // (undocumented)
    readonly?: boolean;
    // (undocumented)
    typeName?: string;
}

// @internal
export class ProjectMember extends WsgInstance {
    // (undocumented)
    email?: string;
    // (undocumented)
    isRole?: boolean;
    // (undocumented)
    name?: string;
    // (undocumented)
    organizationGUID?: string;
    // (undocumented)
    organizationName?: string;
    // (undocumented)
    projectId?: string;
    // (undocumented)
    userId?: string;
}

// @internal (undocumented)
export class ProjectStats extends WsgInstance {
    // (undocumented)
    assigned?: number;
    // (undocumented)
    assignedNearDeadline?: number;
    // (undocumented)
    assignedNew?: number;
    // (undocumented)
    assignedOverdue?: number;
    // (undocumented)
    assignedUpcoming?: number;
    // (undocumented)
    closed?: number;
    // (undocumented)
    count?: number;
    // (undocumented)
    nearDeadline?: number;
    // (undocumented)
    new?: number;
    // (undocumented)
    open?: number;
    // (undocumented)
    overdue?: number;
    // (undocumented)
    upcoming?: number;
}

// @internal (undocumented)
export class WorkflowDefinition extends WsgInstance {
    // (undocumented)
    classification?: string;
    // (undocumented)
    discipline?: string;
    // (undocumented)
    startingTransitions?: WorkflowTransition[];
    // (undocumented)
    states?: WorkflowStatus[];
    // (undocumented)
    transitions?: WorkflowTransition[];
    // (undocumented)
    uninitializedState?: WorkflowStatus;
}


// (No @packageDocumentation comment for this package)

```
