<%*
const file = app.workspace.getActiveFile();
if (file) {
    const today = new Date().toISOString().split('T')[0];
    await app.fileManager.processFrontMatter(file, (fm) => {
        fm.status = "Reading";
        fm.started = today;
    });
}
tR = "";
%>