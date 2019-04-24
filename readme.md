TREpath = [pwd '\results_TRE\'];%TRE结果路径
OPEpath = [pwd '\results_OPE\'];%用于存储OPE结果的路径
fileStruct = dir([TREpath '*.mat']);
for i = 1:length(fileStruct)
    name = fileStruct(i).name;
    load([TREpath name]);
    results = results(1);
    save([OPEpath name],'results');%保存OPE结果到OPE结果路径
end
