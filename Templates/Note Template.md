---
aliases:
createdon: <% tp.date.now("YYYY-MM-DD HH:mm:ss") %>
type:
tags:
---
<%*
//-- Make Sure Every Note has a proper title
let title = tp.file.title
if(title == "Untitled") {
	//-- Prompt for the title
	title = await tp.system.prompt('Enter Note title:');
	//-- Rename the file to the title
	await tp.file.rename(title);
}
%>
# <%- title %>
---
<% tp.file.cursor() %>


## References