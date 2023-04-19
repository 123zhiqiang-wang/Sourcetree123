## v2.1.049 版本更新说明
2022.10.17

## 下载地址
以洛阳服务器为例:目前release的目录已经修改到根目录下，直接在\\192.168.70.12\Software中查找即可，不需要到SVision_Share下
- 软件: \\192.168.70.12\Software\Release\VanGogh\v2.x\v2.1.049
- VG 固件: \\192.168.70.12\SVision_Share\DCC-产品文控中心\VG\电子图纸\固件FIRM WARE
- VG S 固件: \\192.168.70.12\SVision_Share\DCC-产品文控中心\VGS\电子图纸\固件FIRM WARE\MCB\2.1.0

上海服务器改为 \\192.168.50.76\... 即可 
		
## 支持硬件/固件
场内同级硬件都使用最新版本

### MCB
VG：
- HW 4.4.0：FW 4.2.8
- HW 4.3.0 - 4.1.0 : FW 4.2.8，4.2.5
- HW 3.3.0 - 3.0.0 : FW 3.6.0
- HW 2.5.0 ? : FW 0.7.16 ⚠️ 建议尽快升级HW 3或4

VG S：
- HW 1.1.0：FW 2.1.0

### SDB
- HW 4.2.0 - 4.0.0 : FW 4.1.0
- HW 3.3.0 - 3.0.0 : FW 3.1.0
- HW 3.2.0 - 3.0.0 : ⚠️ 建议尽快升级到 HW 3.3.0. 

### SMCB
- HW 2.2.0 : FW 0.7.5，0.7.4

## 升级说明
- 本版本支持VG S MCB FW 2.1.0
- VG S 前后节56°的ScanRangeFactor修改为0.68，此修改不支持自动升级，已出厂的VG S设备，升级软件方法：
  - Step 1: 安装v2.1.049的VG S VanGogh和VanGoghCal
  - Step 2: 打开VanGoghCal，选择Use Rom
  - Step 3: 解密前后节的CalibrationParameters.cfg，修改56°的ScanRangeFactor，保存后加密
  - Step 4: 打开VanGoghCal,选择Use File，升级完毕

## 版本更新说明
### VanGogh
- 数据分析服务器SN: BJ2022060807不支持多个vangogh同时运行
- Alpha-1上capture的时候软件闪退
- 120P 9mm深度 Angio 15x12 1280x1024 R2 HS，tracking off采集完成软件闪退
- Alpha-1 MCB 4.2.8固件，Star 3mm线扫，拖动到左上角capture，会触发安全电路
- FrameTriggerDelay校准完成之后，采数据的时候，log里面有Warning提示：FrameTriggerDelay 481 is not support by MCB firmware
- Acq 120p/220p OffsetChB_mV 设置进04x ECO版本
- v2.1.048 报告打印不全
- star18Line R16 protocol随访出现问题：随访扫描线上不一致
- 历史数据通过菜单load和批量导入无法load：power和mock模式放开限制，customer模式仍然不可以load
- 报告界面患者年龄显示不对
- vanGogh/vanGogh Cal需要支持轴向超高清模式和横向高清模式

### VG S
- VG S 104 Capture刚开始确立reference的时候出现卡顿
- VG S 104人眼tracking on( High Quality) 无rescan情况下，Angio Enface血管和LSO图像上血管有错位
- VGS 线扫长度16时，拖动到左上角，左下角, 需要防御
- VG S 56°，ScanRangeFactor改为0.61之后，导致tracking capture的时候Galvo波形异常
- VG S 增加dummy行扫描
- VGS 销售机客户反馈：对于 配合性差的患者在手动操作时经常容易出现 3分钟弹窗：VG仍保持3min钟弹框，VG S增长到15min

## v2.1.048 版本更新说明
2022.9.2

## 下载地址
以洛阳服务器为例:目前release的目录已经修改到根目录下，直接在\\192.168.70.12\Software中查找即可，不需要到SVision_Share下
- 软件 \\192.168.70.12\Software\Release\VanGogh\v2.x\v2.1.048
- 固件 \\192.168.70.12\SVision_Share\DCC-产品文控中心\VG\电子图纸\固件FIRM WARE

上海服务器改为 \\192.168.50.76\... 即可 
		
## 支持硬件/固件
场内同级硬件都使用最新版本

### MCB
- HW 4.4.0：FW 4.2.8
- HW 4.3.0 - 4.1.0 : FW 4.2.8，4.2.5
- HW 3.3.0 - 3.0.0 : FW 3.6.0
- HW 2.5.0 ? : FW 0.7.16 ⚠️ 建议尽快升级HW 3或4

### SDB
- HW 4.2.0 - 4.0.0 : FW 4.1.0
- HW 3.3.0 - 3.0.0 : FW 3.1.0
- HW 3.2.0 - 3.0.0 : ⚠️ 建议尽快升级到 HW 3.3.0. 

### SMCB
- HW 2.2.0 : FW 0.7.5，0.7.4

## 升级说明
- 本版本支持MCB HW 4.4.0,需要搭配固件4.2.8
- VG S 前后节56°的ScanRangeFactor修改为0.61，此修改不支持自动升级，已出厂的VG S设备，升级软件方法：
  - Step 1: 安装v2.1.048的VG S VanGogh和VanGoghCal
  - Step 2: 打开VanGoghCal，选择Use Rom
  - Step 3: 解密前后节的CalibrationParameters.cfg，修改56°的ScanRangeFactor，保存后加密
  - Step 4: 打开VanGoghCal,选择Use File，升级完毕
- DeltaRefractCorrectOrigin_mm默认值改为-4.2，软件升级有两种方法：
  - 方法一：直接升级，使用参数和老版本一样，对前节要求不高的医院可用此方法升级
  - 方法二：对前节测量精度要求高的医院建议使用此种升级方法
    - Step 1：安装VanGoghCal,选择UseRom
    - Step 2：解密前后节的CalibrationParameters.cfg，修改DeltaRefractCorrectOrigin_mm值为-4.2，修改前节RefractCorrectOrigin_mm的值，在后节Orign的基础上加上-4.2，加密后拷贝到待升级设备上
    - Step 3：打开VanGoghCal，选择UseFile
    - Step 4：重新做前节的轴向畸变校正
   - VG S默认血流授权关闭，如果需要血流授权，需要在授权申请的时候特别说明

## 版本更新说明
### VanGogh
- 045 开EDI导致的OCT Auto Center失败
- 自定义量化工具在research页面也生效
- Research页面第一次计算过ChoroidVessel后，再次load其他数据，不进行计算，打开量化工具会显示量化值
- 在打印报告过程中，快速切换横版和竖版报告，打印出的报告显示不正确
- 手动输入的患者ID中带有下划线符号时，采集的数据在分析页面不显示任何信息
- Patient 列表展示完整版本号
- 00400 v2.1.046报：QThread::start:Failed to set thread priority(参数错误。)
- Live view的时候，OCT和cSSO不对应
- 前节最佳远心 DeltaRefractCorrectOrigin_mm 值设置
- ICL 拱高测量计算优化
- Current auto-working distance (Z axis of 2D stage) has larger variation and failure rate with new pupil illumination LED
- 解决软件闪退
  - 将后节SliceAlign改为false，capture结束后软件闪退
  - 046 capture star protocol之后load数据，软件闪退

### VG S
- VG/VGS cal protocol分开维护，VGS 前节galvo calibration protocol 长度改为10mm x10mm
- VGS high quality tracking眼睛不配合，采集到了部分黑的OCT frame
- VG S 线扫live view的时候，扫描线拖动范围没有做防御
- VGS BackgroundYShift 不对？
- VG S background 电压为正？
- VGS 的ScanRangeFactor 默认值更改

### VGCal
- Check normalized envelope minimum value in VanGoghCal
- 需要将triggerdelay上限值增大
- Dispersion calibration 增加reset功能
- 120p/220P采集卡：确定120p/220P的MinPC Memory
- acq 采集卡inputrange lowgain / highgain 需动态设置
- OCTCal页面Sync选项需要默认选中


## v2.1.045 版本更新说明
2022.7.27

## 下载地址
以洛阳服务器为例:目前release的目录已经修改到根目录下，直接在\\192.168.70.12\Software中查找即可，不需要到SVision_Share下
- 软件 \\192.168.70.12\Software\Release\VanGogh\v2.x\v2.1.045
- 固件 \\192.168.70.12\SVision_Share\DCC-产品文控中心\VG\电子图纸\固件FIRM WARE

上海服务器改为 \\192.168.50.76\... 即可 
		
## 支持硬件/固件
场内同级硬件都使用最新版本

### MCB
- HW 4.3.0 - 4.1.0 : FW 4.2.5
- HW 3.3.0 - 3.0.0 : FW 3.6.0
- HW 2.5.0 ? : FW 0.7.16 ⚠️ 建议尽快升级HW 3或4

### SDB
- HW 4.2.0 - 4.0.0 : FW 4.1.0
- HW 3.3.0 - 3.0.0 : FW 3.1.0
- HW 3.2.0 - 3.0.0 : ⚠️ 建议尽快升级到 HW 3.3.0. 

### SMCB
- HW 2.2.0 : FW 0.7.5，0.7.4

## 升级说明
- VG和VG S软件分开，不同系列产品安装不同软件，然后根据显卡型号选择对应软件版本。3060，3080显卡安装c11版本，其他显卡（1070Ti，RTX 2060, RTX 2060 Super）安装c9版本
- 从v2.1.016-v2.1.045,VG软件支持自动升级，VG S软件不支持自动升级
- 注意事项1：本版本CalibrationParameters 参数DeltaRefArmOrigin_mm默认值更改，从-14.5改为-13。这个改动软件不支持自动升级。 软件升级操作：
  - Step1: 打开VanGoghCal，选择Use Rom
  - Step2：手动修改前节和后节DeltaRefArmOrigin_mm默认值，改为-13
  - Step3: 打开VanGoghCal，Use File
  - Step4：后节打开StepperMotorCal，Home Reference Arm电机，点击Save as orign。
  - Step5: 检查前后节Reference Arm之间的差值是否等于DeltaRefArmOrigin_mm，如果是，检查通过，软件升级完成
- 注意事项2：有些设备出厂的时候DeltaRefArmOrigin_mm默认值已经被手动更改（判断依据：值不是-14.5），这类设备可以直接升级，不需要再做注意事项1的Step1-Step5
- 软件版本的升级必须配合MCB固件版本的升级。升级之后不支持软件版本回退。
	
## 版本更新说明
### VanGogh:
- ACQ采集卡VG部分优化：
  - 集成新采集卡 Acqiris SA120P
  - 安装ACQ采集卡 220p机器，软件开tracking无法采集，报错[Critical] Working thread failed to running in 3000ms!!!
  - Acqiris采集卡需要根据自身的Decimation_ratio参数下发等效的采样频率参数给OCT Calibrator 
  - 配置文件里取消 Decimation_ratio，软件根据 SampleRate_MHz 计算 decimation ratio 然后下发给 Acqiris 采集卡
  - ACQ 220P, SpectrumSamplesPerAScan默认值定义为8640超出了ACQ采集卡AScanSize支持的范围
  - ACQ采集卡，220p tracking 模式为High Quality，无法正常开始采集
  - 220p，High speed模式人眼采集过程中，发生眼动后软件报错，OCT图像上会出现黑带
  - 220P采集卡机器，识别其授权序列号
  - 220p机器，capture页面切换协议以及采集数据过程中OCT图像出现毛刺
  - sa220P liveview Bscan、pattern 间隔 偏长
  - 220p live view卡顿导致auto比较慢，成功率低
  - Angio图像上上有白色亮带（400k+ACQ）
  - ACQ+400K Capture图像出现OCT信号突变，导致angio enface图像上出现黑带
  - 220p acq采集卡机器上启动VG初始化成功后，没有采集数据直接进入到了preview界面

- Smart EDI逻辑改进
  - EDI逻辑改进，增加“默认后节EDI选项”，后节默认打开EDI,前节在晶体模式自动打开EDI
  - EDI逻辑改进Step 2: Reference arm电机随动
  - 后节EDI默认打开，前节开EDI的情况下切换到后节，后节电机位置不对
  - 后节打开EDI的状态下，切换不同的深度，ref arm电机没有随动
  - Smart EDI 导致开EDI后，auto不准

- Tracking速度优化
  - Tracking/set thread priority to highest
  - 适当放宽OCT TrackingMgr 的检查超时时间

- AI标注功能优化：
  - AI标注数据锁定功能
  - AI标注功能中新增四个病灶类别

- 优化abort
  - Fix SW#11410 VGS 操作abort和鼠标中键保存,出现摇杆失联

- 其他功能优化：
  - Follow up采集不下去和采集慢优化
  - 增加中断自动对焦功能
  - 线扫描默认长度修改修改为16mm
  - 保存record 有个百分比显示
  - 建立血流评价标准，在血流协议FAZ评价标准中增加毛细血管清晰度 vSNR 毛细血管连续性 vCont 两项结果
  - 提高FAZ识别的准确性
  - 新增：GCL+ONH复合分析页面
  - ONH/GCL分析页面，没有ONH数据或者只有ONH数据的时候，这个页面上部分信息显示不全
  - 现有青光眼数据库的临时精度提升方案
  - RNFL 厚度低于18岁的按照18岁参考值展示
  - 报告评论区域可输入文字太少，增加到230个字符
  - 报告中医院名字跟患者扫描信息等居中排列
  - 医院院名可输入文字太少
  - 按下打印按钮后，软件无响应
  - 优化：黄斑处 z motion 总是有错位
  - MCB galvo 动态 parking, 改善 repeatability （血流亮线），甚至 Linearity （前节精度）；⚠动态parking功能仅对MCB FW 3.6.0，4.2.5及以上版本开放
  - About中添加完整软件版本号
  - log里面需要给出完整软件版本号
  - 减少log： IVIDigitizer: Size of mat queue is 0, frameIndex 0, patternIndex 1 ？ 输出
  - VG 初始化/关闭软件,live view的时候log有输出parking 日志
  - power模式下:手工分层页面修改分层后，再次load该数据并对分层结果进行reset all操作，切换到angio页面，血流图上显示不正确
  - 修复线扫描协议Line Scan Thickness分析页面计算出来的面积和体积不对
  - GCL Thickness分析页面和报告上Mini改为Min
  - algo page 开放给power
  - 修复 016 6/6.3深度互斥逻辑导致授权不生效
  - 前节ACA分析页面新增：分层线控制按钮
  - 进一步放开SS,AR手动修改限制
  - 前节SS点及晶体前表面识别成功率低
  - 前节未矫正情况下开放测量：增加B-scan without dewarping页面
  - 优化：白内障患者FrameAlign 失败
  - AS Single-line live view的时候可以找到光柱，点了capture之后，光柱明显有个偏移量
  - 修改眼白 英文名 sclera
  - 前节量化数值导出
  - Cube Protocol未矫正情况下开放测量
      
### VG S
  - 增加LSO自动校准功能
  - Monet计算脉络膜厚度
  - VGS-Monet角膜顶点追踪好用
  - VG S StepperMotor参数维护
  - VGS power measurement 策略, 以及 LSO cal 界面 隐藏 power measrement 按钮
  - VG S - VG cal OD/OS 在VG S的StepperMotorCal页面增加OD/OS sensor选项
  - VGS pupil camera 默认参数更改
  - VGS LSO AcquisitionParameters 默认参数更改
  - VGS OCT LaserMZDelta_mm 默认参数更改
  - VGS LSO distortion 默认参数更改
  - VGS_beta2在capture时tracking失败
  - VGS Beta1 VanGoghCal 关闭的时候，有概率出现套接字错误导致的软件闪退

### VanGoghCal
- ACQ采集卡VGCal部分优化：
  - vgcal doesn't support acq digitizer calibration, error code 5
  - 120P色散校正后的值不对
  - ACQ：VanGoghCal ModelConfig中可自动识别采集卡型号，并显示
  - acq 220p采集卡 triggerdelay设置反向了

- VanGoghCal支持中英文切换
- 优化：VanGoghCal的cSSO Calibration中出现了FastLSO的一些参数
- 优化：删除校正参数 psi0、slope 和 C1，由 其他参数进行计算得出并下发
- MCB_FW_3.5.0&4.2.3在不同VGCal版本下 Galvo Test / OCT Galvo Calibration 10mmx10mm输出波形不同
- 对 StepInterval_us 进行校准,在calibrationParameters.cfg里添加一个新的参数，LaserSpeedCorrectionFactor，默认值 1，有效设置防御范围为 0.95~1.05，可调精度 <=0.0005
- 修复旋转 90° 前节 galvo calibration 不准确的问题
- VanGoghCal OCT galvo calibration 需要支持 protocol 90度旋转
- 采集卡 + BD 决定CHA inputrange ，VGCal中加入BD选项
- 新增： VGCal-OCTCal 支持 将envelop提取成mat文件
- VanGoghCal中去掉AnteriorImaging勾选，会重置FrameTriggerDelay参数
- VGcal软件OCT DepthRange开放小数点后4位
- VG CalibrationParameters 参数DeltaRefArmOrigin_mm默认值更改

### VGBurnInTest
- BurnInTest需要支持56度和84度
      
-------------------------------------------------------------------------------------   

## v2.1.016 版本更新说明
2022.6.2

## 下载地址
以洛阳服务器为例 
- 软件 \\192.168.70.12\SVision_Share\Software\Release\VanGogh\v2.x\v2.1.016
- 固件 \\192.168.70.12\SVision_Share\DCC-产品文控中心\VG\电子图纸\固件FIRM WARE

上海服务器改为 \\192.168.50.76\... 即可 
		
## 支持硬件/固件
场内同级硬件都使用最新版本

### MCB
- HW 4.2.0 - 4.1.0 : FW 4.2.3
- HW 3.3.0 - 3.0.0 : FW 3.5.0
- HW 2.5.0 ? : FW 0.7.16 ⚠️ 建议尽快升级HW 3或4

### SDB
- HW 4.2.0 - 4.0.0 : FW 4.1.0
- HW 3.3.0 - 3.0.0 : FW 3.1.0
- HW 3.2.0 - 3.0.0 : ⚠️ 建议尽快升级到 HW 3.3.0. 

### SMCB
- HW 2.2.0 : FW 0.7.5，0.7.4

## 升级说明
- VG和VG S软件分开，不同系列产品安装不同软件，然后根据显卡型号选择对应软件版本。3060，3080显卡安装c11版本，其他显卡（1070Ti，RTX 2060, RTX 2060 Super）安装c9版本
- 从42.7-v2.1.016,VG软件支持自动升级，VG S软件不支持自动升级
- 软件版本的升级必须配合MCB固件版本的升级。升级之后不支持软件版本回退。

	
## 版本更新说明
### VanGogh:
- 优化超广角拼图交互：拼接页面可以进行分析
- 添加log 尝试解决 v1.44.3 capture->abort之后软件闪退 
- 三维扫描数据，扫描区域内空白区域＞10%时有提示 交互修改
- 200-12 的机器， 深度选项逻辑: 6和6.3同时存在的时候，只显示一个
- Angio 12x12 1024x1024 R2 6mm/6G，12mm/8G 显存 capture的时候100%报错
      
### VG S
- VGS SLD 驱动电流上限值改回 133mA

### VanGoghCal
- Alpha-2,220P采集卡，dispersion calibration做好后，正常liveview，有时候PSF会突变 展宽严重
      
--------------------------------------------------------------------------    
## v2.1.014 版本更新说明
2022.5.5

## 下载地址
以洛阳服务器为例 
- 软件 \\192.168.70.12\SVision_Share\Software\Release\VanGogh\v2.x\v2.1.014
- 固件 \\192.168.70.12\SVision_Share\DCC-产品文控中心\VG\电子图纸\固件FIRM WARE

上海服务器改为 \\192.168.50.76\... 即可 
		
## 支持硬件/固件
场内同级硬件都使用最新版本

### MCB
- HW 4.2.0 - 4.1.0 : FW 4.2.3
- HW 3.3.0 - 3.0.0 : FW 3.5.0
- HW 2.5.0 ? : FW 0.7.16 ⚠️ 建议尽快升级HW 3或4

### SDB
- HW 4.2.0 - 4.0.0 : FW 4.1.0
- HW 3.3.0 - 3.0.0 : FW 3.1.0
- HW 3.2.0 - 3.0.0 : ⚠️ 建议尽快升级到 HW 3.3.0. 

### SMCB
- HW 2.2.0 : FW 0.7.5，0.7.4

## 升级说明
- VG和VG S软件分开，不同系列产品安装不同软件，然后根据显卡型号选择对应软件版本。3060，3080显卡安装c11版本，其他显卡（1070Ti，RTX 2060, RTX 2060 Super）安装c9版本
- 从42.7-v2.1.014,VG软件支持自动升级，VG S软件不支持自动升级
- 软件版本的升级必须配合MCB固件版本的升级。升级之后不支持软件版本回退。

	
## 版本更新说明
### VanGogh:
- 通用功能
  - MCB lineparameter cmd逻辑更新问题 fw 3.5.0, 4.2.3，软件对此固件版本做适配。可进一步减少亮线问题
  - 软件速度优化
    - 部分分析页面不提前计算，点击后才计算
    - 分割速度加速及算法加速
    - 优化切换前后节时硬件工作逻辑及顺序
  - 去亮线功能优化
    - fix Tilt frame aligner bug，此bug会导致亮线
    - 解决angio数据边界上亮线识别有误问题
    - Enable tilt Aligner for 15mm ~ 10mm
    - 新的去亮线算法
  - 数据压缩与加密，大大加快数据保存读取速度
    - 数据压缩只针对Cube扫描
    - 开放压缩比配置, 结构和血流分开配置
    - VGCal中禁用数据压缩
  - DCR算法修改：
    - 解决 Alpha-2（100k DCR）图像上方有短竖线
    - 解决 VG S 104数据采集时，在OCT图像上方出现黑带
  - VG支持MCB Smooth jump功能
  - 在VG后台，查询并打印 SLD相关参数
  - 56°/87°部分calibration参数共用
    - 更改84°pupil camera size 参数，并取消84°pupil camera calibration，改为和56°共用calibration 参数
    - 取消84° dispersion calibration，改为和56°共用同一套参数（C2，C3除外）
    - 84°瞳孔相机图像较暗
  - 软件支持MCB_FW_4.2.3 add-on目镜识别功能接口
  - VG支持SA120P 和 SA220P 采集卡
  - Vangogh初始化的时候，先判断pupil camera是否关闭，若是没有关闭，先关闭再打开
  - 新增”打开Log文件“功能
  - AI 标注工具
  - Lite Record 可以保存周期延后到下一次capture开始
  - Liveview protocol pattern的分辨率和main pattern保持一致，并且不能大于512
  - 右键查找record数据对常规模式开放
  - capture with tracking： 3s 采背景只有在rescan的时候判断是否需要执行
  - 非customer模式下，enface增加显示rescan位置功能
  - 批量导入数据功能
  - 关闭自适应后，Bscan图像 zoom in 交互修改
  - 深度授权添加 4.5mm， 生物测量 30 mm
  - VG BurnIn Test迭代结束后，停止live view

- 后节
  - 视网膜分析差异图常规人群范围修改
  - 线扫描协议的line scan thickness页面将光标放在缩略图上，使用键盘上下键切换slice，B-scan图像上的垂直导引线位置不正确
  - 优化 9mm 深度模式下的angio 效果
  - FlowVoid 功能在review模式中开放
  
- 前节
  - 抑制睫状体下方的血流信号
  - 没有晶体前表面的数据分层预测出了晶体前后表面
  - "pIOL-B"点 支持手动增加
  - 角膜校正后图像显示问题

- 超大视野
  - 87度默认协议定义
  - 87Degree模式下，OCTCal Verify Fov失败
  
### Monet
- Monet和前节B Scan分割准确
- 改进前节模型在脉络膜区域的预测稳定性
- 软件中使用模型预测结果代替眼轴分析算法 
- 生物测量-新增分层线控制按钮 
      
### VG S
- VG S tracking速度优化：减弱睫毛遮挡和光斑对tracking的影响
- VG S 第一次启动从双击患者，到Capture页面live view启动需要将近4s的时间
- VG S BurnInTest实现
- VG S设置取消勾选PupilCamera的选项，但看起来并没有生效
- VG S：LSOCal live view的时候关掉VanGoghCal，LSO振镜还在live view
- VG S - VanGogh cal 中MCB页面需要加入VG S相关的FW版本和FPGA版本信息
- VG 和 VG S的auto center的搜索范围分开，VG S Auto center搜索范围[-6,9]，尝试解决VG S auto center容易失败问题
- VG S 去掉Capture页面多余的按钮
- VG S LSO liveview/capture时的分辨率参数修改
- VG S Optical distortion
- VG S LSO 从live view 切换到capture tracking状态，LSO图像Y方向会有shift
- VG S前节optical distortion参数
- VG S 偶发：后节切换深度后，切换前节，眼底图没了
- VG S生物测量设备VG实际深度与显示深度不符
- VG S rescan 消耗时间和 VG 保持一致
- VG S 前/后节 jump speed值修改

### VanGoghCal
- VanGoghCal FrameTriggerDelay 自动校准
- vgcal 支持显示 axial distortion 两个方向，以及 calibration后的效果
- 是否为了解决cSSO图像奇偶行错位严重问题，继续加强算法
      
--------------------------------------------------------------------------    
## v1.42.3-v1.42.7 版本更新说明
2022.4.27

## 下载地址
以洛阳服务器为例 
软件 \\192.168.70.12\SVision_Share\Software\Release\VanGogh\v1.42.7
固件 \\192.168.70.12\SVision_Share\DCC-产品文控中心\VG\电子图纸\Firmware

上海服务器改为 \\192.168.50.76\... 即可 
		
## 支持硬件/固件
场内同级硬件都使用最新版本

### MCB
- HW 4.2.0 - 4.1.0 : FW 4.2.2
- HW 3.3.0 : FW 3.3.0
- HW 3.2.0 : FW 3.3.0
- HW 3.1.0 : FW 3.2.0
- HW 3.0.0 : FW 3.2.0
- HW 2.5.0 ? : FW 0.7.16 ⚠️ 建议尽快升级HW 3或4

### SDB
- HW 4.2.0 - 4.0.0 : FW 4.1.0
- HW 3.3.0 - 3.0.0 : FW 3.1.0, 0.5.8
- HW 3.2.0 - 3.0.0 : ⚠️ 建议尽快升级到 HW 3.3.0. 

### SMCB
- HW 2.2.0 : FW 0.7.5，0.7.4

## 升级说明
	- 需要根据显卡型号安装SetupEnv_v1.42.3，3060显卡安装c11版本，其他显卡安装c9版本
	- VG和VG S软件分开，不同系列产品安装不同软件，然后根据显卡型号选择对应软件版本。比如：VG 2060 Super显卡，安装VG-C9版本
	- 从42.3-42.7,VG软件支持自动升级，VG S软件不支持自动升级

	
## 版本更新说明
### VanGogh:     
    - 通用功能改进：
      - Fix bug：v1.42.3 save数据失败
      - Fix bug：v1.42.3 偶发软件闪退问题
      - Fix bug：v1.42.4bug:连续快速load数据后软件崩溃
      - 优化：Liveview protocol pattern的分辨率和main pattern保持一致，并且不能大于512，缓解9mm深度live view的时候软件卡顿的问题
      
--------------------------------------------------------------------------      
## v1.36.10-v1.42.3 版本更新说明
2022.3.8

## 下载地址
以洛阳服务器为例 
软件 \\192.168.70.12\SVision_Share\Software\Release\VanGogh\v1.42.3
固件 \\192.168.70.12\SVision_Share\DCC-产品文控中心\VG\电子图纸\Firmware

上海服务器改为 \\192.168.50.76\... 即可 
		
## 支持硬件/固件
场内同级硬件都使用最新版本

### MCB
- HW 4.2.0 - 4.1.0 : FW 4.2.2
- HW 3.3.0 : FW 3.3.0
- HW 3.2.0 : FW 3.3.0
- HW 3.1.0 : FW 3.2.0
- HW 3.0.0 : FW 3.2.0
- HW 2.5.0 ? : FW 0.7.16 ⚠️ 建议尽快升级HW 3或4

### SDB
- HW 4.2.0 - 4.0.0 : FW 4.1.0
- HW 3.3.0 - 3.0.0 : FW 3.0.0, 0.5.8
- HW 3.2.0 - 3.0.0 : ⚠️ 建议尽快升级到 HW 3.3.0. 

### SMCB
- HW 2.2.0 : FW 0.7.5，0.7.4

## 升级说明
	- 需要根据显卡型号安装SetupEnv_v1.42.3，3060显卡安装c11版本，其他显卡安装c9版本
	- VG和VG S软件分开，不同系列产品安装不同软件，然后根据显卡型号选择对应软件版本。比如：VG 2060 Super显卡，安装VG-C9版本
	- 从36.10-42.3,VG软件支持自动升级，VG S软件不支持自动升级
	- v1.40.0-v1.42.3不支持自动升级，如需升级到v1.42.3，请联系QA
	
## 版本更新说明
### VanGogh:

    - 通用功能改进：
      - 测量尺，测量面积等通用测量结果保存，不同页面同步
      - 规范导出的“cSSO+Bscan”图像
      - 每次启动和关闭软件的时候，自动进行数据库备份
      - 优化线扫报告，增加竖版报告，优化线扫报告对超级深度图像显示不友好问题
      - 菜单Collect Record选项增加Lite选项，用于Follow up问题数据的收集
      - 菜单增加保持同一深度功能，可以设置后节扫描时的默认深度
      - 分析页面和报告上加入数据深度信息
      
    - 后节：
      - Capture数据存储Motion Correction的结果，对老数据兼容
      - 优化High Speed模式，尝试解决屈光间质差时候的capture卡顿
      - 为多线扫描拟合厚度地形图
      - 体数据增加线扫描页面，支持线扫报告打印
      - 增加独立的RVO、糖网血流分析界面，大视野糖网分析报告
      - 视网膜、GCL厚度分析页面增加正常值显示，增加双眼GCL分析页面
      - Enface分析页面支持分层调整
      - 血流分析页面增加分层线拖动功能
      - 优化脉络膜血管识别算法和显示效果
      - 更新ONH模型，优化ONH分层
      - Mosaic相关功能优化及bug fix:
        - 支持OCT Enface拼接
	- 支持 rvo 糖网模式下的血流拼接
        - 解决Mosaic拼接软件闪图问题
	- 进一步减少Mosaic拼接痕迹

    - 超大视野：
      - 软件支持大视野和超大视野的切换和采集，优化超大视野采集速度
      - 超大视野血流图像显示效果优化
      - 超大视野数据分析性能优化
	
    - 前节：
      - 增加基于瞳孔相机的前节追踪功能
      - 增加前节AR点相关基础测量，改进SS,AR点预测，ACA分析页面开放通用测量工具
      - 增加ICL拱高测量
      - 增加屈光四联图选项，提供角膜前后表面轴向曲率图和前后表面切向曲率图
      - 前节血流显示效果优化：
        - 解决前节血流Max投影过饱和问题
	- 解决前节血流数据图像两侧分层线缺失问题
	- 优化前节血流亮线显示
	- 去除眼表血流信号
	- 前节血流PAR改进
	- 前节血流投射方式改进等
### Monet
    - 眼轴测量分析页面显示信息更全面，支持用户手动调整，可剔除异常值
    - 增加白到白及瞳孔分析页面
	
### VanGoghCal：
    - VGCal中添加PC Memory 配置模块
    - VGCal 增加camera 亮度校准功能
    - VGCal OCT中的signal/clock delay调节范围增大至±40
    - 为87-degree Ocular lens 增加了一些Protocol
    - VanGoghCal中加入新的深度测量校准装置的衰减度测试结果
    - cSSO图像奇偶行错位严重，加强auto delta offset算法
    - add SDB related API information in vgcal-cSSOCal
	
### VG S
    - 集成VG S 后节默认参数到软件中
    - 解决VG S- B-scan 刷新率不稳定问题
    - 优化VG S追踪，在有光斑的情况下减少追踪次数
    - VG S - live view时候需要降低B-scan中A-scan 的密度，从而提升live view速度以及Auto速度
    - 软件支持 VG S- OD/OS 需求
    - 解决VG S软件稳定性部分问题：
      - VG S capture过程中abort，软件live view没有恢复，后续都无法capture了
      - 点击Capture页面上Focus电机上下箭头键，VG S Focus电机卡顿
      - VG S上同一个exe，多次启动，启动的时候会有概率崩溃
      - VG S多次采集过程中报错
      - VG S按手柄的采集连续两次，点击abort不起作用
      - VG S DC上电后立刻开启VG S Cal,经常会遇到Fail to connect to VGS-board 的问题
      - VG S VG cal中 cSSO/LSO live状态下启动motor，LSO会freeze
    - 为VG S 提供Use Rom支持
    
--------------------------------------------------------------------------	
## v1.36.2-v1.36.10 版本更新说明
2022.2.28

## 软件下载地址
	上海服务器下载地址：\\192.168.50.76\SVision_Share\Software\Release\VanGogh\v1.36.10
	洛阳服务器下载地址：\\192.168.70.12\SVision_Share\Software\Release\VanGogh\v1.36.10

## 支持固件
	- MCB  3.3.0
	- SDB  0.5.8, 3.3.0, 4.4.0
	- SMCB 0.7.4, 0.7.5
## 升级说明
	- 软件支持从v1.36.2直接升级到v1.36.10
## 版本更新说明

### Vangogh:
	- 菜单项：VanGogh中添加控制环形照明灯的开关
	- 菜单项：Bscan auto拉伸显示的默认值，由设置参数控制
	- 优化惠普激光打印机报告打印速度
	- 优化：恢复部分被删除的protocol
	- 优化：体数据 对比和OU模式关闭 Auto BSCAN
	- 优化：切换前后节增加camera的re-start逻辑，来解决整机爆发"相机捕获"失败和上电丢失问题
	- 优化：通过放松Search Range，加强auto delta offset算法，以减少cSSO图像奇偶行错位严重问题
	- Fix bug：9350采集卡前节模式inputrange默认设置不对
	- Fix bug：Thorlabs激光器OCT Noise Level Test不对导致的软件闪退
	- Fix bug：青光眼钟点图TISA 均值有问题
	- Fix bug：平均之后的slice 视网膜区域出现毛刺
### VanGoghCal：
        - MCBCal里加一个save按钮，可以保存环形照明灯的电流
	- VanGoghCal中加入深度测量校准装置的衰减度测试结果
	- Fix bug：cSSOCal中点击reset to default按钮后save会导致前节的轴向畸变校正的值被重置
	
	
## v1.32.9-v1.36.2 版本更新说明
2021.8.13

## 软件下载地址
	上海服务器下载地址：\\192.168.50.76\SVision_Share\Software\Release\VanGogh\v1.36.2
	洛阳服务器下载地址：\\192.168.70.12\SVision_Share\Software\Release\VanGogh\v1.36.2

## 支持固件
	- MCB  3.3.0
	- SDB  0.5.8
	- SMCB 0.7.4
## 升级说明
	- 安装VanGogh和VanGoghCal
	- 打开VanGoghCal，选择USE ROM，后节模式打开StepperMotorCal,OCT Lens Switch电机点击Save as Origin按钮
	- 需要使用前节校准工装再做前节的Galvo Calibration和Axial Distortion Calibration
	- 升级完毕，卸载VanGoghCal
## 版本更新说明
### Vangogh:
	- 优化UI
	- 新增数据库导出导出功能
  #### 后节
	- 新增Fovea自动识别功能
	- 新增根据眼轴长度调整图像放大倍数的功能
	- 新增无灌注面积识别功能
	- 优化FAZ识别算法，增加手动调整和数值导出功能
	- 优化通用测量工具与特殊测量工具交互
	- 优化后节ColorBar
	- 优化软件右上角设置
  #### 前节：
	- 前节capture页面数据采集改进
		- 新增：Live view时自动找光柱
		- 新增：焦平面可视化，方便采集
		- 新增：EDI自动shift参考臂，即开关EDI，前节图像在UI上的位置不变
	- 前节分析功能
		- 新增前节屈光四联图
		- 新增前节enface，血流分析页面
		- 新增SS点自动识别和量化
		- 新增角膜上皮厚度地形图
		- 优化前节分层
	- 优化：前节图像平均改进，AS Single-line R64协议图像模糊问题得到很大改善
### VanGoghCal：
	- VanGoghCal支持100k，200k双速度校准
	- VanGoghCal添加前节轴向畸变修正
	- VanGoghCal前节Galvo Calibration校准
	
## 遗留问题
	- 前节血流图像过饱和，血流图像上存在亮线
	- 前节分层：在角膜缺失的数据上，分层线和图像不贴合
	- VG Mock Hardeware Version默认200D，replay 100D样机采集的数据，报DCR input parameters not correct
	- ModelConfig中修改Model Dependent Data中的内容不点击Apply Profile按钮，会重置配置文件，更新EEPROM
	
