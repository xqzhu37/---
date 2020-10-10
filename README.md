第一步：
单个提交
cellranger count进行细胞计数和转录组比对并生成特征条形码矩阵，bsub < J1_2.lsf
#BSUB -J count
#BSUB -n 10
#BSUB -R span[hosts=1]
#BSUB -o %J0_2.count.out
#BSUB -e %J0_2.count.err
#BSUB -q normal
#/public/home/xqzhu/bin/bin/cellranger count  
module load cellranger/4.0.0
cellranger count --id=J1_2 --sample=J1_2-1,J1_2-2,J1_2-3,J1_2-4,J1_2-5,J1_2-6,J1_2-7,J1_2-8,J1_2-9,J1_2-10,J1_2-11,J1_2-12  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/J1_2

多个提交
#!/bin/sh
module load cellranger/4.0.0
bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count --id=J1_2 --sample=J1_2-1,J1_2-2,J1_2-3,J1_2-4,J1_2-5,J1_2-6,J1_2-7,J1_2-8,J1_2-9,J1_2-10,J1_2-11,J1_2-12,J1_2-13,J1_2-14,J1_2-15,J1_2-16  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/J1_2"

bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count --id=J12_1 --sample=J12_1-1,J12_1-2,J12_1-3,J12_1-4,J12_1-5,J12_1-6,J12_1-7,J12_1-8,J12_1-9,J12_1-10,J12_1-11,J12_1-12,J12_1-13,J12_1-14,J12_1-15,J12_1-16  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/J12_1"

bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count --id=J6_1 --sample=J6_1-1,J6_1-2,J6_1-3,J6_1-4,J6_1-5,J6_1-6,J6_1-7,J6_1-8  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/J6_1"
bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count  --id=J6_2 --sample=J6_2-1,J6_2-2,J6_2-3,J6_2-4,J6_2-5,J6_2-6,J6_2-7,J6_2-8  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/J6_2"
bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count --id=J12_2 --sample=J12_2-1,J12_2-2,J12_2-3,J12_2-4,J12_2-5,J12_2-6,J12_2-7,J12_2-8,J12_2-9,J12_2-10,J12_2-11,J12_2-12  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/J12_2"
bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count --id=T1_1 --sample=T1_1-1,T1_1-2,T1_1-3,T1_1-4,T1_1-5,T1_1-6,T1_1-7,T1_1-8  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/T1_1"
bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count --id=T6_1 --sample=T6_1-1,T6_1-2,T6_1-3,T6_1-4,T6_1-5,T6_1-6,T6_1-7,T6_1-8,T6_1-9,T6_1-10,T6_1-11,T6_1-12  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/T6_1"
bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count --id=T6_2 --sample=T6_2-1,T6_2-2,T6_2-3,T6_2-4,T6_2-5,T6_2-6,T6_2-7,T6_2-8,T6_2-9,T6_2-10,T6_2-11,T6_2-12  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/T6_2"

bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count --id=T12_2 --sample=T12_2-1,T12_2-2,T12_2-3,T12_2-4,T12_2-5,T12_2-6,T12_2-7,T12_2-8  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/T12_2"
bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count --id=T12_1 --sample=T12_1-1,T12_1-2,T12_1-3,T12_1-4,T12_1-5,T12_1-6,T12_1-7,T12_1-8  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/T12_1"
bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count --id=T1_2 --sample=T1_2-1,T1_2-2,T1_2-3,T1_2-4,T1_2-5,T1_2-6,T1_2-7,T1_2-8,T1_2-9,T1_2-10,T1_2-11,T1_2-12,T1_2-13,T1_2-14,T1_2-15,T1_2-16  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/T1_2"
bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count --id=T0_2 --sample=T0_2-1,T0_2-2,T0_2-3,T0_2-4,T0_2-5,T0_2-6,T0_2-7,T0_2-8,T0_2-9,T0_2-10,T0_2-11,T0_2-12  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/T0_2"
bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count --id=J0_2 --sample=J0_2-1,J0_2-2,J0_2-3,J0_2-4,J0_2-5,J0_2-6,J0_2-7,J0_2-8,J0_2-9,J0_2-10,J0_2-11,J0_2-12  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/T6_2" 
bsub -J count -n 10 -R span[hosts=1] -o %J.out -e %J.err -q normal "cellranger count --id=T0_1 --sample=T0_1-1,T0_1-2,T0_1-3,T0_1-4,T0_1-5,T0_1-6,T0_1-7,T0_1-8,T0_1-9,T0_1-10,T0_1-11,T0_1-12  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/T0_1"
