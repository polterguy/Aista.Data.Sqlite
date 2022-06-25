
# Aista.Data.Sqlite

Port of Microsoft.Data.Sqlite. This repository only exists for one single reason, which is that the default NuGet package Microsoft
has published for Microsoft.Data.Sqlite doesn't respect foreign keys if you use `DbCommend.ExecuteScalar` or its async version
to insert items with a tail of ` returning *`, which is a problem for us as Aista since we're dependent upon such functionality
to have our own things work. Once Microsoft publishes a new (stable) package of Microsoft.Data.Sqlite with this feature, we will
archive this repository, and archive its associated NuGet package. However for the time being, we need such features to have
a stable product ourselves, so for the time being to fix this problem, we forked their code, fixed the problem, and created this
repository to replace Microsoft's primary SQLite data adapter.

