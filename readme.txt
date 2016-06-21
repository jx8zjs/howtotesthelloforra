opt -instnamer -mem2reg -break-crit-edges test1.bc -o test1.bcc

opt -load ../llvm-3.7.1.src/cmakebuild/lib/vSSA.so -vssa test1.bcc -o test1.essa.bcc

opt -load ../llvm-3.7.1.src/cmakebuild/lib/RangeAnalysis.so -load ../llvm-3.7.1.src/cmakebuild/lib/LLVMHello.so -VarRangeToolPass test1.essa.bcc > /dev/null


