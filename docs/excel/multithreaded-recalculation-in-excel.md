---
title: Excel でのマルチ スレッド再計算
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- thread-safe cells [excel 2007],multithreading in Excel,concurrent tasks [Excel 2007],thread-safe functions [Excel 2007],multithreaded recalculation [Excel 2007],MTR [Excel 2007],XLL functions [Excel 2007], registering as thread safe,recalculation [Excel 2007], multithreaded,memory contention [Excel 2007],registering XLL functions as thread safe [Excel 2007],unsafe functions [Excel 2007]
localization_priority: Normal
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 010a1029e0bf5ba1a36b324ebd402f6e90603fb9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798933"
---
# <a name="multithreaded-recalculation-in-excel"></a>Excel でのマルチ スレッド再計算

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Office Excel 2007 �́A���[�N�V�[�g�̃}���`�X���b�h�Čv�Z (MTR) �g�p���� Excel �̍ŏ��̃o�[�W�����ł����B�R���s���[�^�[�̃v���Z�b�T����v���Z�b�T�̃R�A���Ɋ֌W�Ȃ��A�Čv�Z���ɍő� 1024 �̓������s�X���b�h��g�p����悤�� Excel ��\���ł��܂��B 
  
> [!NOTE]
> [!����] ���ꂼ��̃X���b�h�ɂ͊֘A����I�y���[�e�B���O �V�X�e���̃I�[�o�[�w�b�h�����邽�߁A�K�v�ȏ�ɑ����̃X���b�h��g�p����悤�� Excel ��\�����Ă͂����܂���B 
  
�R���s���[�^�[�ɕ����̃v���Z�b�T�܂��̓v���Z�b�T�̃R�A�����ڂ���Ă���ꍇ�́A�I�y���[�e�B���O �V�X�e�����A�œK�ȕ��@�Ńv���Z�b�T�ɃX���b�h����蓖�Ă܂��B
  
## <a name="excel-mtr-overview"></a>Excel の MTR の概要

Excel �́A�v�Z�`�F�[���̊e�����̂����A�ʁX�̃X���b�h�ŕ��s�I�ɍČv�Z�ł��镔������ʂ��悤�Ƃ��܂��B���̔��ɒP���ȃc���[ (x �� y �́Ay �� x �ɂ݈̂ˑ����Ă��邱�Ƃ�Ӗ�����) �́A���̗������Ă��܂��B
  
**�} 1. �ʁX�̃X���b�h�ł̓������s�v�Z**

![異なるスレッドで同時に計算します。](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "異なるスレッドで同時に計算します。")
  
A1 �̌v�Z���ςނƁA����̃X���b�h�ł� A2�AA3 �̏��Ɍv�Z���ł���悤�ɂȂ�A�����ɁA�������̃X���b�h�ł� B1�AC1 �̏��Ɍv�Z���ł���悤�ɂȂ�܂� (���ׂẴZ�����X���b�h �Z�[�t�ł���Ɖ��肵�Ă��܂�)�B 
  
> [!NOTE]
> [!����] �X���b�h �Z�[�t�ȃZ���Ƃ����p��́A�X���b�h �Z�[�t�Ȋ֐��݂̂�܂ރZ����Ӗ����܂��B�X���b�h �Z�[�t�ł��邩�ǂ����ɂẮA[Excel �ŃX���b�h �Z�[�t�ƌ��Ȃ������ (���Ȃ���Ȃ����)](#xl2007xllsdk_threadsafe)�ŏڂ���������܂��B 
  
�قƂ�ǂ̎��p�I�ȃu�b�N�ɂ́A���̗����͂邩�ɕ��G�Ȉˑ��֌W�c���[���܂܂�Ă��܂��B����ɁA�Z���̍Čv�Z�ɂ����鎞�Ԃ͌v�Z����������܂ŕs���ł���A�֐��̈����ɂ���đ啝�ɈقȂ邱�Ƃ�����܂��B�ŗǂ̌��ʂ𓾂邽�߂ɁAExcel �́A����ȏ�̍œK�����ł��Ȃ��Ȃ�܂ŁA�v�Z�̂��тɌv�Z�����̉��P����݂܂��B
  
Excel �́A���̍��ڂ̎��s�ɒP��̃��C�� �X���b�h��g�p���܂��B
  
- �g�ݍ��݃R�}���h
    
- XLL �R�}���h
    
- XLL アドイン マネージャー インターフェイスの関数 (**xlAutoOpen**関数というように) 
    
- Microsoft Visual Basic for Applications (VBA) �̃��[�U�[��`�R�}���h (�ʏ�̓}�N���ƌĂ΂�܂�)
    
- VBA �̃��[�U�[��`�֐�
    
- �g�ݍ��݂̃X���b�h �Z�[�t�ł͂Ȃ����[�N�V�[�g�֐� (���̃Z�N�V�����Ɉꗗ������܂�)
    
- XLM マクロ シートのユーザー定義コマンドとユーザー定義関数
    
- COM �A�h�C���̃R�}���h�Ɗ֐�
    
- ����t���t�H�[�}�b�g����̊֐��Ɖ��Z�q
    
- ワークシートの式で使用された定義済みの名前定義内の関数と演算子
    
- �����ҏW�{�b�N�X��̎��̋����I�ȕ]�� ( **F9** �L�[��g�p) 
    
���ׂẴ��[�N�V�[�g�̐����́A�֐����X���b�h �Z�[�t���ǂ����Ɋ֌W�Ȃ��A���C�� �X���b�h�ŕ]������܂��B�������A�����̃X���b�h��g�p����悤�� Excel ��\�����Ă���ꍇ������܂��B���[�U�[�������̃X���b�h��g�p����悤�Ɏw�肷��ƁA�X���b�h �Z�[�t�̃Z���ɂ͒ǉ��̃X���b�h���g�p����܂��B���ו��U�̊ϓ_����̍������ɓK���ꍇ�́A���C�� �X���b�h��X���b�h �Z�[�t�ȃZ���Ɏg�p����܂��B
  
�����ł����x�������ׂ����ƂƂ��āAExcel �͈�x�ɕ����̃R�}���h����s���܂���B���̂��߁A�X���b�h ���[�J�� �������ƃN���e�B�J�� �Z�N�V�����̎g�p�ȂǁA�X���b�h �Z�[�t�Ȋ֐���L�q����Ƃ��Ɠ��l�̒��ӂ𕥂��K�v�͂���܂���B
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a>何し、は見なされませんスレッド セーフ Excel を使用して
<a name="xl2007xllsdk_threadsafe"> </a>

Excel �ł́A���̂�̂������X���b�h �Z�[�t�ƌ��Ȃ���܂��B
  
- Excel �̒P�����Z�q�Ɠ񍀉��Z�q�̂��ׂ�
    
- Excel 2007 �ȍ~�̑g�ݍ��݃��[�N�V�[�g�֐��̂قƂ�ǂ��ׂ� (��O�̈ꗗ��Q��)
    
- �X���b�h �Z�[�t�Ƃ��Ė����I�ɓo�^����Ă��� XLL �A�h�C���֐�
    
���̑g�ݍ��݃��[�N�V�[�g�֐��́A�X���b�h �Z�[�t�ł͂���܂���B
  
- **PHONETIC**
    
- **CELL** ("����" �܂��� "�A�h���X" �̂ǂ��炩�̈������g�p���ꂽ�ꍇ) 
    
- **INDIRECT**
    
- **GETPIVOTDATA**
    
- **CUBEMEMBER**
    
- **CUBEVALUE**
    
- **CUBEMEMBERPROPERTY**
    
- **CUBESET**
    
- **CUBERANKEDMEMBER**
    
- **CUBEKPIMEMBER**
    
- **CUBESETCOUNT**
    
- **ADDRESS** (5 �Ԗڂ̃p�����[�^�[ "sheet_name" ���w�肳��Ă���ꍇ) 
    
- データベースのいずれかのピボット テーブルを参照する関数 (**DSUM**、 **DAVERAGE**というように)
    
- **エラーです。タイプ**
    
- **HYPERLINK**
    
���m�ɂ��邽�߂ɁA�X���b�h �Z�[�t�ƌ��Ȃ���Ȃ���̂�����܂��B
  
- VBA �̃��[�U�[��`�֐�
    
- COM �A�h�C���̃��[�U�[��`�֐�
    
- XLM �}�N�� �V�[�g�̃��[�U�[��`�֐�
    
- �����I�ɃX���b�h �Z�[�t�Ƃ��ēo�^����Ă��Ȃ� XLL �A�h�C���֐�
    
���̑���Ɗ֐��̓X���b�h �Z�[�t�Ƃ͌��Ȃ���܂���B�܂��A�X���b�h �Z�[�t�Ƃ��ēo�^���� XLL �֐�����Ăяo�����Ǝ��s���܂��B
  
- 呼び出しを XLM 情報関数では、たとえば、 **xlfGetCell** (**取得します。セル**)。
    
- **XlfSetName** (**SET.NAME**) を定義または xll ファイルの内部名を削除する場合に呼び出されます。
    
- �X���b�h �Z�[�t�ł͂Ȃ����[�U�[��`�֐��� **xlUDF** ��g�p�����Ăяo���B
    
- 式のスレッドの安全でない関数が含まれているかの定義には、スレッドの安全でない関数が含まれている定義済みの名前が含まれている[xlfEvaluate](xlfevaluate.md)関数を呼び出します。 
    
- �u���[�N�����N���A���� [xlAbort](xlabort.md) �֐��̌Ăяo���B 
    
- �v�Z����Ă��Ȃ��Z���̎Q�Ƃ̒l��擾���� [xlCoerce](xlcoerce.md) �֐��̌Ăяo���B 
    
> [!NOTE]
> [!����] XLL ���[�N�V�[�g�֐� ( **xlcSave** �Ȃ�) �ł́AC API �R�}���h�̌Ăяo����������Ă��܂���B���̊֐����X���b�h �Z�[�t�Ƃ��ēo�^����Ă��邩�ǂ����͊֌W����܂���B 
  
�X���b�h �Z�[�t�Ƃ��Đ錾���ꂽ XLL �֐��� XLM ���֐���Ăяo���Ȃ����Ƃ�A�v�Z����Ă��Ȃ��Z����Q�Ƃł��Ȃ����Ƃ���AExcel �� �}�N�� �V�[�g�Ɠ����Ƃ��ēo�^���� XLL �֐���X���b�h �Z�[�t�Ƃ��Ă�o�^���邱�Ƃ�����܂���B���̂��߁A **xlCoerce** ��g�p���Čv�Z����Ă��Ȃ��Z���̎Q�Ƃ̒l��擾���悤�Ƃ���ƁA **xlretUncalced** �G���[�Ŏ��s���܂��BXLM ���֐��̌Ăяo���́A **xlretFailed** �G���[�Ŏ��s���܂��B���̑��̑O�q�����|�C���g�́AExcel C API �ɓ������ꂽ�G���[ �R�[�h **xlretNotThreadSafe** �Ŏ��s���܂��B 
  
C API ��p�̃R�[���o�b�N�֐��́A���ׂăX���b�h �Z�[�t�ł��B
  
- **xlCoerce** (�������A�v�Z����Ă��Ȃ��Z���̎Q�Ƃ̋����^�ϊ��͎��s���܂�) 
    
- **xlFree**
    
- **xlStack**
    
- **xlSheetId**
    
- **xlSheetNm**
    
- **xlAbort** (�u���[�N�����N���A���邽�߂Ɏg�p����ꍇ������܂�) 
    
- **xlGetInst**
    
- **xlGetHwnd**
    
- **xlGetBinaryName**
    
- **xlDefineBinaryName**
    
�B��̗�O�� **xlSet** �֐��ł��B�����̏ꍇ�A���̊֐��̓R�}���h�Ɠ����ł��邽�߁A�ǂ̂悤�ȃ��[�N�V�[�g�֐������Ăяo���ł��܂���B 
  
XLL ���[�N�V�[�g�֐��́A�X���b�h �Z�[�t�Ƃ��� Excel �ɓo�^�ł��܂��B����ɂ��A���̊֐������S�ɕ����̃X���b�h�œ����ɌĂяo���邱�Ƃ� Excel �ɒʒm���܂��B�������A���ꂪ�����ł��邱�Ƃ͎����Ŋm�F����K�v������܂��B�X���b�h �Z�[�t�Ƃ��ēo�^�����֐��̓��삪�X���b�h �Z�[�t�łȂ��ƁAExcel ���s����ɂȂ邱�Ƃ�����܂��B
  
## <a name="registering-xll-functions-as-thread-safe"></a>としてスレッド セーフな XLL 関数を登録します。
<a name="xl2007xllsdk_threadsafe"> </a>

�X���b�h �Z�[�t�Ȋ֐���L�q����Ƃ��ɁA�J���҂��]���K�v�̂��郋�[���͎��̂Ƃ���ł��B
  
- �X���b�h �Z�[�t�ł͂Ȃ��\���̂���ʂ� DLL ��̃��\�[�X��Ăяo���Ȃ��B
    
- C API �܂��� COM ��ʂ��ăX���b�h �Z�[�t�łȂ��Ăяo����s��Ȃ��B
    
- �N���e�B�J�� �Z�N�V������g�p���āA�����̃X���b�h�œ����Ɏg�p�����\���̂��郊�\�[�X��ی삷��B
    
- �X���b�h�ŗL�̃X�g���[�W�ɂ̓X���b�h ���[�J�� ��������g�p���āA�֐���̐ÓI�ϐ��̓X���b�h ���[�J���ϐ��ɒu��������B
    
Excel �ɂ́A��� 1 �̐������ۂ����܂��B�X���b�h �Z�[�t�Ȋ֐���}�N�� �V�[�g�Ɠ����Ȃ�̂Ƃ��ēo�^���邱�Ƃ͂ł��܂���B���̂��߁AXLM ���֐���Ăяo�����Ƃ�A�Čv�Z����Ă��Ȃ��Z���̒l��擾���邱�Ƃ͂ł��܂���B
  
## <a name="memory-contention"></a>メモリの競合
<a name="xl2007xllsdk_threadsafe"> </a>

�}���`�X���b�h �V�X�e���́A2 �̊�{�I�Ȗ��ɑΏ�����K�v������܂��B
  
- �����̃X���b�h���ǂݏ������郁�����̕ی���@�B
    
- ���s���̃X���b�h�Ɋ֘A�t�����ăv���C�x�[�g�ɂȂ郁�����̍쐬���@�ƃA�N�Z�X���@�B
    
Windows �I�y���[�e�B���O �V�X�e���� Windows �\�t�g�E�F�A�J���L�b�g (SDK) �ɂ́A����痼���ɂ��ꂼ��Ή�����c�[���ł���N���e�B�J�� �Z�b�V�����ƃX���b�h ���[�J�� �X�g���[�W (TLS) API ��g�p�ł��܂��B�ڍׂɂ��ẮA�u[Excel �̃������Ǘ�](memory-management-in-excel.md)�v��Q�Ƃ��Ă��������B
  
�ŏ��̖��́A���Ƃ��΁A2 �̃��[�N�V�[�g�֐� (�܂��͓����֐��� 2 �̓������s�C���X�^���X) �� 1 �� DLL �v���W�F�N�g��̃O���[�o���ϐ��ɃA�N�Z�X���� (�܂��͕ύX�������) �K�v������ꍇ�ɔ������܂��B���̂悤�ȃO���[�o���ϐ��́A�O���[�o���ɃA�N�Z�X�ł���N���X �I�u�W�F�N�g�̃C���X�^���X��ɉB����Ă��邱�Ƃ�����_�ɒ��ӂ��K�v�ł��B
  
2 �ڂ̖��́A���Ƃ��΁A���[�N�V�[�g�֐����֐��{�̂̃R�[�h��ŐÓI�ȕϐ��܂��̓I�u�W�F�N�g�錾���Ă���ꍇ�ɔ������܂��BC/C++ �R���p�C���́A���ׂẴX���b�h���g�p���� 1 �̃R�s�[�݂̂�쐬���܂��B���̂��߁A�֐��̈���̃C���X�^���X���l��ύX���Ă���Ƃ��ɁA�ʂ̃X���b�h�̂������̃C���X�^���X�͒l���ȑO�ɐݒ肳�ꂽ��e���Ƒz�肵�Ă���\��������Ƃ������Ƃł��B
  
## <a name="example-applications-of-mtr"></a>MTR のサンプル アプリケーション
<a name="xl2007xllsdk_threadsafe"> </a>

���[�N�V�[�g�֐���G�N�X�|�[�g���� XLL �́AExcel �̃}���`�X���b�h�Čv�Z (MTR) �𗘗p�ł��܂� (�Y������֐����A�X���b�h �Z�[�t�łȂ��A�N�V��������s����K�v���Ȃ��ꍇ)�B����ɂ��AExcel �̓u�b�N��\�Ȍ���Z���ԂɍČv�Z�ł���悤�ɂȂ邽�߁A������A�v���P�[�V�����ɂƂ��Ė]�܂�����ԂɂȂ�܂��B
  
具体的には、MTR は、ユーザー定義関数 (Udf) 目的の結果を取得する外部プロセスを呼び出すこと自体を呼び出しているブックの再計算時間に大きな影響を及ぼします。 具体的には、UDF を同時に多数の要求を処理できるリモート サーバーを呼び出すと関数呼び出しを含むブックを検討してください。 ブックの再計算がシングル スレッドの場合、各 UDF を呼び出すし、リモート サーバーにする必要があります完了次のいずれかをする前に。 これは、一度に多数の呼び出しを処理するサーバーの能力を浪費します。 ブックの再計算は、マルチ スレッドは、同時にまたは連続で、Excel は複数の呼び出しをことができます。
  
�T�[�o�[�Ɠ����� (���̐��� N �Ƃ���) �̃X���b�h��g�p����悤�� Excel ���\������Ă��āA�u�b�N�̈ˑ��֌W�c���[�̃g�|���W�ɂ��̗]�n������΁A���v�̍Čv�Z���Ԃ̓V���O�� �X���b�h�̌v�Z���Ԃ� 1/N �߂��܂ŒZ�k�����\��������܂��B����́A�u�b�N����s���Ă���N���C�A���g �R���s���[�^�[���v���Z�b�T�� 1 �������ڂ��Ă���ꍇ�ɂ���Ă͂܂�\��������܂��B���ɁA�T�[�o�[�̌Ăяo���ɂ����鎞�Ԃ��A�T�[�o�[�ŌĂяo����������鎞�Ԃ���Z���ꍇ�ɓ��Ă͂܂�܂��B 
  
�ǉ��̃X���b�h�ɂ́A���ꂼ��ɃI�y���[�e�B���O �V�X�e���̃I�[�o�[�w�b�h�����݂��܂��B���̂��߁A����̃u�b�N�Ɠ���̃T�[�o�[����уN���C�A���g �R���s���[�^�[�ɂ��āA���炩�̎����� Excel �ɐݒ肷��œK�ȃX���b�h���������K�v������܂��B 
  
���Ƃ��΁AExcel ����s���Ă���V���O�� �v���Z�b�T�̃R���s���[�^�[�ƁA1,000 �̃Z����܂�ł���u�b�N�ɂ��čl���Ă݂܂��傤�B����́AUDF ��Ăяo���A���� UDF �� 1 �ȏ�̃����[�g �T�[�o�[��Ăяo���܂��B1,000 �̃Z�������݂Ɉˑ����Ă��Ȃ��Ɖ��肷��ƁAExcel �͌㑱�̌Ăяo������s���邽�߂ɌĂяo���̊�����ҋ@����K�v�͂���܂��� (���̐���́A���̗�ɉe����^���邱�ƂȂ��A������x�̊ɘa���\�ł�)�B�T�[�o�[�� 100 ���̗v���̓����������\�ŁAExcel �� 100 �X���b�h��g�p����悤�ɍ\������Ă���ƁA���s���Ԃ� 1 �X���b�h�݂̂�g�p�����ꍇ�� 1/100 �߂��ɂ܂ŒZ�k�ł��܂��BExcel ���e�X���b�h�ɃZ������蓖�Ă邽�߂ɂ�����I�[�o�[�w�b�h�ƁA�I�y���[�e�B���O �V�X�e���� 100 �X���b�h��Ǘ����邽�߂ɂ�����I�[�o�[�w�b�h�ɂ��A���ۂɂ́A����قǂ܂ł̎��ԒZ�k�ɂ͂Ȃ�܂���B�܂��A�T�[�o�[�̃X�P�[�����O���K�؂ł���A100 ���̃^�X�N�̓���������˗����Ă�ʂ̃^�X�N�̊������Ԃɑ傫�ȉe�����Ȃ��Ƃ������Ƃ�A�ÖٓI�ɉ��肵�Ă��܂��B
  
���̋Z�@���傫�ȃ����b�g�ɂȂ���p�I�A�v���P�[�V�����Ƃ��āA�����e�J�����@�ȂǁA�����ȃ^�X�N�ɕ������ĕ����̃T�[�o�[�Ɉ˗��ł��鐔�l�W��^�̃^�X�N���������܂��B
  
## <a name="excel-services-considerations"></a>Excel Services に関する考慮事項
<a name="xl2007xllsdk_threadsafe"> </a>

Excel Services �́A�T�[�o�[�ł� Excel �X�v���b�h�V�[�g�̓ǂݍ��݁A�v�Z�A����у����_�����O��T�|�[�g���܂��B���[�U�[�́A�W���̃u���E�U �c�[����g�p���āA�X�v���b�h�V�[�g�ɃA�N�Z�X���đΘb�������s�ł���悤�ɂȂ�܂��B
  
Excel Services �� UDF �́AMicrosoft .NET Framework �̃}�l�[�W �R�[�h��g�p���č쐬��, .NET �A�Z���u����ʂ��Ďg�p�\�ɂȂ�܂��BXLL �́AExcel Services �ł̓T�|�[�g����܂���B�}�l�[�W �R�[�h �T�[�o�[ UDF ���\�[�X�́AXLL ��Ăяo���Ă��̋@�\�ɃA�N�Z�X�ł��邽�߁A���[�U�[�̓T�[�o�[�œǂݍ��܂ꂽ�u�b�N�ƃN���C�A���g�œǂݍ��܂ꂽ�u�b�N�œ����@�\��g�p�ł��܂��B
  
���̕��@�� XLL �̊֐���g�p�ł���悤�ɂ���ɂ́A�����Ɩ߂�l��l�C�e�B�u �f�[�^�^���� .NET Framework �}�l�[�W �f�[�^�^�ɕϊ����� XLL �֐���Ăяo�� .NET �A�Z���u���ŁA�֐�����b�v����K�v������܂��B.NET ���b�p�[�́A�A�N�Z�X�Ώۂ� XLL �֐����Ƃ� 1 �̃T�[�o�[ UDF ��G�N�X�|�[�g���܂��B�ǉ��̗v���Ƃ��āA���̕��@�ŌĂяo����� XLL �֐��̓X���b�h �Z�[�t�ł��邱�Ƃ��K�v�ł��BXLL �֐��͖{���̕��@�� Excel �ɓo�^����Ă��Ȃ����߁A���̊֐�������I�ɃX���b�h �Z�[�t�ɂ�����@���T�[�o�[�� .NET ���b�p�[�ɂ͂���܂���B����́AXLL �J���҂̐ӔC�ŕۏ؂��܂��B
  
## <a name="see-also"></a>�֘A����

- [Excel �̍Čv�Z](excel-recalculation.md)  
- [Excel �̃������Ǘ�](memory-management-in-excel.md) 
- [Excel �� XLL �R�[�h�ɃA�N�Z�X����](accessing-xll-code-in-excel.md)  
- [Excel �v���O���~���O�̊T�O](excel-programming-concepts.md)  
- [Excel XLL SDK API �֐����t�@�����X](excel-xll-sdk-api-function-reference.md)

