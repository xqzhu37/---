第一步：cellranger count进行细胞计数和转录组比对并生成特征条形码矩阵
#BSUB -J count
#BSUB -n 10
#BSUB -R span[hosts=1]
#BSUB -o %J0_2.count.out
#BSUB -e %J0_2.count.err
#BSUB -q normal
#/public/home/xqzhu/bin/bin/cellranger count  
module load cellranger/4.0.0
cellranger count --id=J1_2 --sample=J1_2-1,J1_2-2,J1_2-3,J1_2-4,J1_2-5,J1_2-6,J1_2-7,J1_2-8,J1_2-9,J1_2-10,J1_2-11,J1_2-12  --transcriptome=/public/home/xqzhu/cellranger_reference/Ghirsutum  --fastqs=/data/cotton/Rawdata/Rawdata/J1_2
