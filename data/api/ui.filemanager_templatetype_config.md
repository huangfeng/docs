templateType
=============

@short:
	specifies the type of a file

@type: function
@example:
templateType: function templateType(obj) {
	var types = webix.i18n.filemanager.types;
	return types && types[obj.type] ? types[obj.type] : obj.type;
}

@template:	api_config
@descr:


