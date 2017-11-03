'use strict';

var Zap = {

create_pre_write: function(bundle) {

bundle.action_fields.Name = bundle.action_fields.Customer_Name;
delete bundle.action_fields.Customer_Name;
bundle.request.data = JSON.stringify(bundle.action_fields);

return bundle.request;

}
};
