<%*
const file = app.workspace.getActiveFile();
if (file) {
    await app.fileManager.processFrontMatter(file, (fm) => {
        fm.volumes_read = (Number(fm.volumes_read) || 0) + 1;
    });
}
tR = "";
%>