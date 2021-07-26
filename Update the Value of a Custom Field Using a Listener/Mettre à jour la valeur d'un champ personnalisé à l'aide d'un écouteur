import com.atlassian.jira.component.ComponentAccessor
import com.atlassian.jira.issue.ModifiedValue
import com.atlassian.jira.issue.util.DefaultIssueChangeHolder

// the name of the custom field to update
final customFieldName = 'TextFieldA'

// the new value of the field
final newValue = 'I love Groovy !'

def customFieldManager = ComponentAccessor.customFieldManager
def issue = event.issue

def customField = customFieldManager.getCustomFieldObjects(issue).findByName(customFieldName)
assert customField : "Could not find custom field with name $customFieldName"

customField.updateValue(null, issue, new ModifiedValue(issue.getCustomFieldValue(customField), newValue), new DefaultIssueChangeHolder())
