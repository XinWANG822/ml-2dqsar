��������Դ��ChEMBL17���ݿ⣬ɸѡ����Ϊtarget_type = 'SINGLE PROTEIN', assay_type = 'B'��

�����ݰ������¼����ļ����ļ��У�
1��compounds.txt	����compounds��chembl_id�б�
2��compounds_7.txt	����compounds��chembl_id�б�ɸѡ����Ϊconfidence_score >= 7
3��targets.txt	����compounds��chembl_id�б�
4��targets_7.txt	����targets��chembl_id�б�ɸѡ����Ϊconfidence_score >= 7
5��compounds_properties.txt	����compounds�������б�
	molecule_chembl_id
	MOLREGNO	NUMBER(9,0)	NOT NULL	Foreign key to compounds table (compound structure)
	MW_FREEBASE	NUMBER(9,2)		Molecular weight of parent compound
	ALOGP	NUMBER(9,2)		Calculated ALogP
	HBA	NUMBER(3,0)		Number hydrogen bond acceptors
	HBD	NUMBER(3,0)		Number hydrogen bond donors
	PSA	NUMBER(9,2)		Polar surface area
	RTB	NUMBER(3,0)		Number rotatable bonds
	RO3_PASS	VARCHAR2(3)		Indicates whether the compound passes the rule-of-three (mw < 300, logP < 3 etc)
	NUM_RO5_VIOLATIONS	NUMBER(1,0)		Number of violations of rule-of-five
	MED_CHEM_FRIENDLY	VARCHAR2(3)		Indicates whether the compound is considered Med Chem friendly (Y/N)
	ACD_MOST_APKA	NUMBER(9,2)		The most acidic pKa calculated using ACDlabs v12.01
	ACD_MOST_BPKA	NUMBER(9,2)		The most basic pKa calculated using ACDlabs v12.01
	ACD_LOGP	NUMBER(9,2)		The calculated octanol/water partition coefficient using ACDlabs v12.01
	ACD_LOGD	NUMBER(9,2)		The calculated octanol/water distribution coefficient at pH7.4 using ACDlabs v12.01
	MOLECULAR_SPECIES	VARCHAR2(50)		Indicates whether the compound is an acid/base/neutral
	FULL_MWT	NUMBER(9,2)		Molecular weight of the full compound including any salts
	AROMATIC_RINGS	NUMBER(3,0)		Number of aromatic rings
	HEAVY_ATOMS	NUMBER(3,0)		Number of heavy (non-hydrogen) atoms
	NUM_ALERTS	NUMBER(3,0)		Number of structural alerts (as defined by Brenk et al., ChemMedChem 2008)
	QED_WEIGHTED	NUMBER(3,2)		Weighted quantitative estimate of drug likeness (as defined by Bickerton et al., Nature Chem 2012)
	UPDATED_ON	DATE		Shows date properties were last recalculated
	MW_MONOISOTOPIC	NUMBER(11,4)		Monoisotopic parent molecular weight
	FULL_MOLFORMULA	VARCHAR2(100)		Molecular formula for the full compound (including any salt)
	natural_product
	standard_inchi_key
	canonical_smiles
6��targets_properties.txt ����targets�������б�
	target_chembl_id
	PROTEIN_CLASS_ID	NUMBER(9,0)	NOT NULL	Primary key. Unique identifier for each classification.
	PROTEIN_CLASS_DESC	VARCHAR2(410)	NOT NULL	Concatenated description of each classification for searching purposes etc.
	L1	VARCHAR2(50)	NOT NULL	First level classification (e.g., Enzyme, Transporter, Ion Channel).
	L2	VARCHAR2(50)		Second level classification.
	L3	VARCHAR2(50)		Third level classification.
	L4	VARCHAR2(50)		Fourth level classification.
	L5	VARCHAR2(50)		Fifth level classification.
	L6	VARCHAR2(50)		Sixth level classification.
	L7	VARCHAR2(50)		Seventh level classification.
	L8	VARCHAR2(50)		Eighth level classification.
7��compounds_targets_interaction_7.txt	����compounds��targets�����ü�¼��ɸѡ����Ϊconfidence_score >= 7
	molecule_chembl_id
	target_chembl_id
	standard_value	��λΪnm
	confidence_score
8��targets_compounds�ļ���	ÿ���ļ����ļ�����targets��chembl_id�����м�¼�����䷴Ӧ������compounds��chembl_id��ɸѡ����Ϊconfidence_score >= 7