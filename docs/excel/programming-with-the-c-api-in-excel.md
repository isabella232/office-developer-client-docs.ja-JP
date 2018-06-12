---
title: Excel �ł� C API ��g�p�����v���O���~���O
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007],programming interfaces [Excel 2007],C API [Excel 2007], when to use,C API [Excel 2007], relation to XLM,Excel programming interfaces
localization_priority: Normal
ms.assetid: 142bc0ce-7d16-4b69-9799-ce6558da2def
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 459e57d41ef7497c535e51944bbaf24daee84167
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798939"
---
# <a name="programming-with-the-c-api-in-excel"></a>Excel �ł� C API ��g�p�����v���O���~���O

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel 2013 XLL �\�t�g�E�F�A�J���L�b�g�� C API ��g�p���āAExcel 2013 �̍��p�t�H�[�}���X�̃��[�N�V�[�g�֐���쐬�ł��܂��BExcel 2013 �� C API �ւ̃A�b�v�O���[�h�́A�T�[�h �p�[�e�B���@�\�܂��͓���@�\�̃p�t�H�[�}���X���d�v�ȈӖ�������[�U�[�ɑ΂��Čp�����čs���Ă���T�|�[�g�𔽉f���܂��B
  
## <a name="excel-programming-interfaces"></a>Excel �̃v���O���~���O �C���^�[�t�F�C�X

Excel �ɂ́A�C���^�[�t�F�C�X��g�p���� Excel �Ɛڑ�����A�v���P�[�V������J�����邽�߂̂������̃I�v�V�������p�ӂ���Ă��܂��BExcel �̃v���O���~���O �C���^�[�t�F�C�X�́A���̏����ňȑO�̃o�[�W�����ɒǉ�����܂����B
  
- **XLM �}�N������:** Excel �̊g���@�\�̂��߂Ƀ��[�U�[���g�p�ł���ŏ��̌���ŁAC API �̊�b�ɂȂ�܂����BXLM �́AExcel 2010 �ł�T�|�[�g����Ă��܂������A���Ȃ�ȑO�� Visual Basic for Applications (VBA) �ɒu���������܂����B 
    
- **C API �� XLL:** Excel �ɓ�������Ă��� DLL �ł��B������ DLL �́A���p�t�H�[�}���X�̃��[�N�V�[�g�֐���ǉ�����ł���ړI�ōő��̃C���^�[�t�F�C�X��񋟂��܂��B�������A����ȍ~�̋Z�p�Ɣ�r���Ă����炩���G�ł��B 
    
- **VBA:** Excel �u�b�N �I�u�W�F�N�g�Ɋ֘A�t�����Ă��� Visual Basic �R�[�h �I�u�W�F�N�g�ł��BVBA �́A�C�x���g �g���b�v�A�J�X�^�}�C�Y�A���[�U�[��`�֐��ƃR�}���h�̒ǉ���\�ɂ��Ă��܂��BVBA �́A�ł��ʓI�Ɏg�p����A�ł�e�Ղɗ��p�ł���g���I�v�V�����ł��B 
    
- **COM:** Windows �x�[�X�̃A�v���P�[�V���������̑��݉^�p���̕W���ł��BExcel �́A������ăC�x���g��I�u�W�F�N�g����J���܂��BVBA �́ACOM ��g�p���� Excel �ƑΘb���܂��BExcel �́A�O������ Excel �𐧌䂷�� C++ COM �R�[�h�̃��\�[�X��A�v���P�[�V������쐬����̂ɖ𗧂� COM �^�C�v ���C�u������G�N�X�|�[�g���܂��B 
    
- **Microsoft .NET Framework:** ���U���̐v���ȃA�v���P�[�V�����J���p�ɐ݌v���ꂽ�A��������}�l�[�W �R�[�h���ł��B.NET Framework �����̃R�[�h�̎�v�ȃv���O���~���O����� C# �ł����A�����̌���� Microsoft ���Ԍ��� (MSIL) �ɃR���p�C���ł��܂��BExcel 2013 �ł�, .NET Framework �A�Z���u���Ɋ܂܂��R�[�h ���\�[�X�ɃA�N�Z�X�ł��܂��B 
    
## <a name="when-to-use-the-c-api"></a>C API ��g�p����ꍇ

Xll を記述し、C API を使用する主な理由としては、高性能なワークシート関数を作成します。 XLL 関数は、ユーザー定義関数、Xll にする技術のほとんどのユーザーは現実的ではありませんを記述するために必要なスキルと知識を取得する時間の投資とも呼ばれます。 関数の高パフォーマンスのアプリケーションではそれにもかかわらず、- と Excel 2013、強力なサーバー リソースをマルチ スレッドのインターフェイスを記述する機能、これを Excel の機能拡張の非常に重要な一部にします。 
  
Excel 2007 �œ������ꂽ C API �̉����́A���[�U�[ �C���^�[�t�F�C�X�Ȃǂ̋@�\�ł͂Ȃ��A��ɍ����\�Ȍv�Z�Ɋ֘A���鑤�ʂɊ֌W���Ă��܂��B
  
### <a name="writing-high-performance-user-defined-worksheet-functions"></a>���p�t�H�[�}���X�̃��[�U�[��`���[�N�V�[�g�֐��̍쐬

XLL �A�h�C����쐬���āA���p�t�H�[�}���X�̃��[�N�V�[�g�֐���쐬����ꍇ�AExcel �� C API �͗��z�I�ȑI����ł��BC API ��g�p����ƁA���[�N�V�[�g�̃f�[�^�֍ł���ړI�ɃA�N�Z�X�ł��܂��BXLL ��g�p����ƁAExcel �� DLL ���\�[�X�֍ł���ړI�ɃA�N�Z�X�ł���悤�ɂȂ�܂��BExcel 2013 �ł́A�V�����f�[�^�^���ǉ�����邱�Ƃɂ���āA�܂��ł�d�v�Ȃ��ƂƂ��āA�N���X�^�[�����ꂽ�T�[�o�[�ł̃��[�U�[��`�֐��̎��s���T�|�[�g����邱�Ƃɂ���āAXLL �̃p�t�H�[�}���X�͂���Ɍ��サ�Ă��܂��B
  
XLL �̎g�p�ɂ̓R�X�g��������܂��BC API �ɂ́AVBA�ACOM, .NET Framework �ɂ���A���Ȃ荂���x���̐v���ȊJ���@�\�͂���܂���B�������Ǘ��͒჌�x���ōs����̂ŁA�J���҂ɂ��傫�ȐӔC�𕉂킹�邱�ƂɂȂ�܂��BCOM �o�R�Ō��J����Ă��鑽���� Excel �@�\�́AVBA ��.NET Framework ���ė��p�ł��܂����AC API �ɂ͌��J����Ă��܂���B
  
### <a name="accessing-multithreaded-servers-by-using-xll-worksheet-functions"></a>XLL ���[�N�V�[�g�֐���g�p�����}���`�X���b�h �T�[�o�[�ւ̃A�N�Z�X

Excel 2007 で導入された、マルチ スレッド再計算 (MTR) を使用すると、スレッド セーフな XLL ワークシート関数を作成できます。マルチ スレッド サーバーにアクセスするのに、これらの関数を使用できます。以下のセクションでは、ユーザーが観察するパフォーマンスをどのように大幅に向上させることができるかを詳細に説明します。処理能力を大量に消費する必要がある Excel ユーザーに対して、MTR を使用する XLL と強力な計算サーバーの組み合わせは、最高のパフォーマンス ソリューションを提供します。
  
### <a name="customizing-the-excel-user-interface"></a>Excel ���[�U�[ �C���^�[�t�F�C�X�̃J�X�^�}�C�Y

Excel �̑����̃o�[�W�����ł́AC API �̓��[�U�[ �C���^�[�t�F�C�X��J�X�^�}�C�Y����ۂɁA�œK�ȑI����ł͂���܂���ł����BVBA �́AExcel �̃I�u�W�F�N�g�ƃC�x���g�ւ̃A�N�Z�X�ɗD��Ă��܂��BExcel 2007 �œ������ꂽ���[�U�[ �C���^�[�t�F�C�X�́A�O�ςƊ�{�Z�p�̗��ʂŁA�ȑO�̃o�[�W�����Ƃ͑傫���قȂ�܂��B�}�l�[�W �R�[�h�̃��\�[�X��g�p���āA���̃C���^�[�t�F�C�X��œK�ɃJ�X�^�}�C�Y�ł��܂��B
  
### <a name="creating-applications-that-can-be-accessed-on-the-internet"></a>�C���^�[�l�b�g��ŃA�N�Z�X�\�ȃA�v���P�[�V�����̍쐬

2007 Microsoft Office system �œ������ꂽ Excel Services �ł́A�W���� Web �u���E�U�[ �c�[����g�p���āA���[�U�[���u�b�N�� Excel �̋@�\�ɃA�N�Z�X����őP�̕��@��񋟂��܂��B.NET Framework �J������ƃ��\�[�X�Ƌ��ɁA�����̋Z�p�͏����ɓn���ă��[�U�[�ɂƂ��� Excel �W�J�̏d�v�ȕ����ɂȂ�܂��B
  
### <a name="controlling-excel-from-external-applications"></a>�O���A�v���P�[�V��������� Excel �̐���

Excel �́A���̃I�u�W�F�N�g�A���\�b�h�A�C�x���g�� COM �C���^�[�t�F�C�X�o�R�Ō��J���܂��B���������āAExcel �Z�b�V������J�n���Đ��䂵����A������ Excel �Z�b�V�����𐧌䂵���肷��X�^���h�A���� �A�v���P�[�V������쐬���邽�߂� COM ��g�p�ł��܂��BC++ �� VBA ��܂ށA�������̊J������� COM �Ɍ��J����Ă��� Excel �C���^�[�t�F�C�X�ɃA�N�Z�X�ł��܂��BC# �� .NET Framework �ł́A���l�� Excel �ւ̃����[�g �A�N�Z�X�Ɛ����\�ɂ��� Excel �ւ̃C���^�[�t�F�C�X��񋟂��܂��B
  
## <a name="asynchronous-calling-of-excel"></a>Excel �̔񓯊��Ăяo��

Excel �� XLL �ɐ������łɓn���Ă���ꍇ�ɂ̂݁AXLL �� C API ��Ăяo�����Ƃ��ł���悤�ɂ��܂��BExcel ���Ăяo�����[�N�V�[�g�֐��́AC API ��g�p���� Excel �ɃR�[���o�b�N�ł��܂��BExcel ���Ăяo�� XLL �R�}���h�́AC API ��Ăяo�����Ƃ��ł��܂��BVBA ���ꎩ�̂� Excel �ɂ���ČĂяo�����Ƃ��� VBA ���Ăяo�� DLL�AXLL �֐��A�R�}���h�́AC API ��Ăяo�����Ƃ��ł��܂��B���Ƃ��΁A���Ԏw��� Windows �R�[���o�b�N�� XLL �ɐݒ肵�A���� XLL ���� C API ��Ăяo�����Ƃ͂ł��܂���B�܂��AXLL �ɂ���č쐬���ꂽ�o�b�N �O���E���h �X���b�h���� C API ��Ăяo�����Ƃ�ł��܂���BDLL �܂��� XLL ���� COM ��g�p���Ĕ񓯊��� Excel ��Ăяo�����Ƃ͂����߂ł��܂���B
  
�C�x���g�ɔ񓯊��ɉ������� Excel �̃A�v���P�[�V����������ꍇ�A����ɂ͑����̐���������܂��B���Ƃ��΁AExcel ���C���^�[�l�b�g��̃f�[�^�̈ꕔ��擾���A�f�[�^���ύX����邽�тɍČv�Z����悤�ɂ������Ƃ��܂��B���邢�́A�o�b�N�O���E���h �X���b�h�Ōv�Z����s���A���̏I������ Excel ���Čv�Z����悤�ɂ������ꍇ�����܂��B
  
Excel ���ύX��A�N�e�B�u�Ƀ|�[�����O����悤�ɂ���Ύ����ł��܂����A����� Excel ���p�ɂɒʏ�̏����𒆒f����̂Ō����I�ł͂���܂��񂵁A����������܂��B���z�I�ȃ\�����[�V�����ł͂���܂��񂪁AC API �܂��� VBA ��g�p���āA���Ԏw��ŌJ��Ԃ��R�}���h��ݒ肷�邱�Ƃ�ł��܂��B
  
理想的には、データの変更を検出し、Excel をトリガーして更新の取得と再計算を実行させる、より効率的な外部プロセスが望まれます。COM を使用して Excel とインターフェイスを介して接続するアプリケーションを使用することによって、これを実現できます。Excel が明示的に制御を渡す場合にのみ呼び出す C API と同じような制限は COM にはありません。ダイアログボックスが表示されていたり、メニューがプルダウンされていたり、マクロが実行されている場合は、メソッドの呼び出しは無視されます。しかし、Excel が準備完了状態のときにはいつでも、COM アプリケーションは Excel メソッドを呼び出すことができます。
  
## <a name="c-api-and-its-relation-to-xlm"></a>C API �� XLM �Ƃ̊֌W

Excel �}�N�� (XLM) ����́AExcel �Œ񋟂��ꂽ�A���[�U�[�����p�ł���ŏ��̃v���O���~���O���ł����B���[�U�[�́A�ʏ�̃��[�N�V�[�g�Ɏ��Ă�����ʂȃ}�N�� �V�[�g�ŁA�Ǝ��̃R�}���h��֐���쐬�ł��܂����BExcel 2013 �ł�A�������� XLM �}�N�� �V�[�g���T�|�[�g����Ă��܂��B **SUM** �� **LOG** �Ȃǂ̒ʏ�̃��[�N�V�[�g�֐����ׂĂ�}�N�� �V�[�g�Ŏg�p�ł��܂��B����Ƀ��[�N�V�[�g�ɓ��͂��邱�Ƃ͂ł��Ȃ����̍��ڂ�}�N�� �V�[�g�ł͎g�p�ł��܂��B 
  
- ���[�N�X�y�[�X���֐� ( **GET.CELL**�A **GET.WORKBOOK** �Ȃ�)�B
    
- �ʏ�̃��[�U�[����̎�������\�ɂ���A�R�}���h�Ɠ����̊֐� ( **DEFINE.NAME**�A **PASTE** �Ȃ�)�B
    
- �A�h�C���Ɋ֘A����֐� ( **REGISTER** �Ȃ�)�B
    
- �R�}���h�Ɠ����̃C�x���g �g���b�v ( **ON.ENRTY**�A **ON.TIME** �Ȃ�)�B
    
- �}�N���֐��ŗL�̑��� ( **ARGUMENT**�A **VOLATILE** �Ȃ�)�B
    
- �t���[���䑀�� ( **GOTO**�A **RETURN** �Ȃ�)�B
    
Excel �o�[�W���� 3 �ɂ́AC API �̋@�\�����ł����݂��܂��B�������AExcel �o�[�W���� 4 �ł́AXLM ���ꂪ C API �Ƀ}�b�v����Ă��܂����B����ȍ~�ADLL �͂��ׂẴ��[�N�V�[�g�֐��A�}�N�� �V�[�g���֐��A�R�}���h�A�C�x���g �g���b�v�̐ݒ��Ăяo�����Ƃ��\�ɂȂ�܂����BDLL �́AC API ������� XLM �t���[����֐���Ăяo�����Ƃ͂ł��܂���B�����̃}�N�� �V�[�g�֐��ƃR�}���h�́A�w���v �t�@�C�� XLMacr8.hlp (�ȑO�� Macrofun.hlp �Ƃ������O�ł���) �ɋL�ڂ���Ă��܂��B���̃w���v �t�@�C������肷��ɂ́A�u[Microsoft �_�E�����[�h �Z���^�[](http://download.microsoft.com)�v�Ɉړ����A"XLMacr8.hlp" ��������܂��B 
  
> [!NOTE]
> [!����] Windows Vista �� Windows 7 �́A���ڂɂ� .hlp �t�@�C����T�|�[�g���Ă��܂���B�������A���̃t�@�C����J�����Ƃ̂ł��� [Windows Vista �p�� Windows �w���v �v���O���� (WinHlp32.exe)]([](http://go.microsoft.com/fwlink/?LinkID=82148)�A[Windows 7 �p�� Windows �w���v �v���O���� (WinHlp32.exe)](http://www.microsoft.com/download/en/details.aspx?id=91) �� Microsoft ����_�E�����[�h�ł��܂��B 
  
DLL �́A�R�[���o�b�N�֐� **Excel4**�A **Excel4v**�A **Excel12**�A **Excel12v** (�Ō�� 2 �́AExcel 2007 �œ������ꂽ) ��g�p���āA�֐��ƃR�}���h�ɑΉ����� C API ��Ăяo���܂��B�e�֐��ƃR�}���h�ɑΉ�����񋓌^�̒萔�́A�w�b�_�[ �t�@�C���Œ�`����A������ 1 �Ƃ��Ă����̃R�[���o�b�N�ɓn����܂��B���Ƃ��΁A **xlfGetCell** �ɑΉ����� **GET.CELL**�A **xlfRegister** �ɑΉ����� **REGISTER**�A **xlcDefineName** �ɑΉ����� **DEFINE.NAME** �ł��B
  
���[�N�V�[�g�֐��A�}�N�� �V�[�g�֐��A�R�}���h��񋟂��邱�Ƃɉ����āAC API �� DLL ����炱���̃R�[���o�b�N��g�p���邱�Ƃɂ���Ă̂݌Ăяo�����Ƃ��ł���֐��ƃR�}���h�̗񋓑̂�񋟂��܂��B���Ƃ��΁A **xlGetName** �́ADLL �� Excel �Ɋ֐��ƃR�}���h��o�^����ꍇ�ɕK�v�Ƃ���ADLL ���̂̊��S�p�X�ƃt�@�C��������o�ł���悤�ɂ��܂��B 
  
Excel �o�[�W���� 5 �ł� Visual Basic for Applications (VBA) �V�[�g�̓����A�o�[�W���� 8 (Excel 97) �ł� Visual Basic Editor (VBE) �̓����ȍ~�A���[�U�[�� Excel ��J�X�^�}�C�Y����ł�e�Ղȕ��@�́AXLM �̑���� VBA ��g�p���邱�Ƃł��B���������āAExcel �̂���ȍ~�̃o�[�W�����œ������ꂽ�V�����@�\�̑����́AXLM �܂��� C API ���Ăł͂Ȃ� VBA ���ė��p�ł��܂��B���Ƃ��΁A�������̃R�}���h�A�C�x���g �g���b�v�A�g���_�C�A���O �{�b�N�X�@�\�́AXLM �܂��� C API ���Ăł͂Ȃ��AVBA ���ė��p�ł��܂��B
  
�ڂ����́A�u[Excel �p C API �̐V�@�[](what-s-new-in-the-c-api-for-excel.md)(what-s-new-in-the-c-api-for-excel.md)�v��������������B
  
## <a name="see-also"></a>�֘A����



[Excel �p C API �̐V�@�[](what-s-new-in-the-c-api-for-excel.md)(what-s-new-in-the-c-api-for-excel.md)
  
[C API �R�[���o�b�N�֐� Excel4�AExcel12](c-api-callback-functions-excel4-excel12.md)


[Excel XLL SDK �̊T�v](getting-started-with-the-excel-xll-sdk.md)

