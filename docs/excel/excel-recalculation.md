---
title: Excel �̍Čv�Z
manager: kelbow
ms.date: 03/09/2018
ms.audience: Developer
ms.topic: overview
keywords:
- forced calculation [excel 2007],selective recalculation [Excel 2007],functions [Excel 2007], volatile,calculation modes,recalculated cells [Excel 2007],dependence [Excel 2007],specified worksheet calculation [Excel 2007],recalculation [Excel 2007],workbook tree rebuild [Excel 2007],range calculation [Excel 2007],Excel recalculation,volatile functions [Excel 2007],functions [Excel 2007], non-volatile,active worksheet calculation [Excel 2007],dirty cells [Excel 2007],non-volatile functions [Excel 2007],forced recalculation [Excel 2007]
localization_priority: Normal
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 9964f2c4282158e83891d82ba43fa19f23ab1eb6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798844"
---
# <a name="excel-recalculation"></a>Excel �̍Čv�Z

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel �̍Čv�Z�́A�����̕��@�Ńg���K�[�ł��܂��B���ɁA���̗������܂��B
  
- �V�����f�[�^����͂��� (Excel ���A���̃g�s�b�N�Ő�����鎩���v�Z���[�h�̏ꍇ)�B
    
- �u�b�N�̈ꕔ�܂��͂��ׂĂ̍Čv�Z�� Excel �ɖ����I�Ɏw������B
    
- �s�܂��͗��폜�܂��͑}������B
    
- **[�ۑ��O�ɍČv�Z]** �I�v�V������I���ɂ��Ă���Ƃ��Ƀu�b�N��ۑ�����B 
    
- ����� [�I�[�g�t�B���^] �̃A�N�V��������s����B
    
- �s�܂��͗�̋�؂����_�u���N���b�N���� (�����Čv�Z���[�h��)�B
    
- ��`���ꂽ���O��ǉ��A�ҏW�A�܂��͍폜����B
    
- ���[�N�V�[�g�̖��O��ύX����B
    
- �ʂ̃��[�N�V�[�g�Ƃ̑��Έʒu��ύX����B
    
- ��ł͂Ȃ��A�s���\���܂��͍ĕ\������B
    
> [!NOTE]
> [!����] ���̃g�s�b�N�ł́A���[�U�[�����ڃL�[���������}�E�X��N���b�N�����肷�邱�ƂƁA�R�}���h��}�N���ɂ���ĊY������^�X�N�����s����邱�Ƃ��ʂ��܂���B���[�U�[�̓R�}���h����s���邩�A���炩�̑���ɂ���ăR�}���h�����s�����悤�ɂ��܂����A����̓��[�U�[ �A�N�V�����ƌ��Ȃ���܂��B���̂��߁A�u���[�U�[�v�Ƃ����t���[�Y�́A�u���[�U�[�A�܂��̓��[�U�[�ɂ���ĊJ�n���ꂽ�R�}���h�܂��̓v���Z�X�v�Ƃ����Ӗ��ɂ�Ȃ�܂��B 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a>�ˑ��֌W�A�_�[�e�B �Z���A����эČv�Z�����Z��

Excel �̃��[�N�V�[�g�̌v�Z�́A3 �i�K�̃v���Z�X�ƌ��Ȃ��܂��B
  
1. �ˑ��֌W�c���[�̍\�z
    
2. �v�Z�`�F�[���̍\�z
    
3. �Z���̍Čv�Z
    
依存関係ツリーによって、Excel は、セル間の依存関係または同等性、セル間の参照関係についての情報を得ます。Excel は、このツリーから計算チェーンを構築します。計算チェーンは、数式を格納しているすべてのセルの一覧であり、計算される順序で並べられています。再計算時に、まだ計算されていないセルに依存する数式が見つかると、このチェーンは Excel によって改訂されます。この場合、計算されるセルとそのセルの参照先は、チェーンの末尾方向に移動されます。このため、開いた直後のワークシートでの最初の数回の計算サイクルは、多くの場合、計算時間が向上します。
  
構造上の変更が行われたとき、ブックに、新しい数式が入力されると、Excel には、依存関係ツリーおよび計算チェーンが再構築します。 新しいデータまたは新しく作成した数式が入力されると、Excel が再計算を必要とすると新しいデータに依存するすべてのセルをマークします。 この方法でマークされているセルは、*ダーティ*と呼ばれます。 すべての直接的および間接的な依存関係はダーティとマークされては A1、B1、C1 は、A1 が変更されたとき、B1 とは異なります。 場合は、B1 と C1 の両方がダーティとして設定できるようにします。 
  
あるセルがそのセル自体に直接的または間接的に依存している場合は、Excel によって循環参照が検出され、ユーザーに警告が示されます。これは、通常ユーザーが修正しなければならないエラー状態です。Excel には、ユーザーが循環依存の関係の原因を見つけられるようにする非常に役立つグラフィカルなナビゲーション ツールがあります。場合によっては、この状態を意図的に必要とすることもあります。たとえば、次の繰り返しの開始点が、前の繰り返しの結果になる反復計算の実行を必要とすることがあります。Excel は、[計算方法の設定] ダイアログ ボックスによる反復計算の制御をサポートしています。
  
セルにダーティのマークを付けた後、次回の再計算が実行されるときに、Excel は、それぞれのダーティ セルの内容を計算チェーンで指定された順序で再評価します。前述の例では、最初に B1、次に C1 の順になります。この再計算は、再計算モードが自動になっている場合には、Excel がセルにダーティのマークを付け終わった直後に実行されます。それ以外の場合は、再計算は後で実行されます。
  
Microsoft Excel 2002 �ȍ~�� Microsoft Visual Basic for Applications (VBA) �� **Range** �I�u�W�F�N�g�́A�Z���Ɍv�Z���K�v�Ƃ����}�[�N��t���� **Range.Dirty** ���\�b�h��T�|�[�g���Ă��܂��B���̃��\�b�h�� **Range.Calculate** ���\�b�h�ƕ��p����� (���̃Z�N�V������Q��)�A����͈͓̔�̃Z��������I�ɍČv�Z�ł���悤�ɂȂ�܂��B����́A�v�Z���[�h���蓮�ɐݒ肳��Ă���Ƃ��ɁA�}�N���Ō���I�Ȍv�Z����s����ۂɁA���̃}�N���֐��Ƃ͖��֌W�̃Z����v�Z����I�[�o�[�w�b�h������邽�߂ɖ𗧂��܂��B�͈͌v�Z�̃��\�b�h�́AC API �ł͎g�p�ł��܂���B 
  
Excel 2002 �ȑO�̃o�[�W������ Excel �ł́A�J���Ă���e�u�b�N�̃��[�N�V�[�g���ƂɌv�Z�`�F�[����\�z���Ă��܂����B���̂��߁A��������郏�[�N�V�[�g�Ԃ̃����N���@�͕��G�ɂȂ�A�����I�ȍČv�Z�̂��߂ɂ͒��ӂ��K�v�ł����B���� Excel 2000 �ł́A���[�N�V�[�g�Ԃ̈ˑ��֌W��ŏ����ɂ��āA���[�N�V�[�g�ɃA���t�@�x�b�g���̖��O��t����K�v������܂��B���̂悤�ɂ��āA���̃V�[�g�Ɉˑ�����V�[�g���A�ˑ���̃V�[�g�̌�� (�A���t�@�x�b�g��) �Ȃ�悤�ɂ��܂��B
  
Excel 2007 では、計算チェーンのセクションが相互に依存していないし、同時に計算することができますように、複数のスレッドで再計算を有効にするロジックが改良されました。 マルチプロセッサまたはマルチコア コンピューターで、シングル プロセッサ コンピューター上の複数のスレッドまたは 1 つのスレッドを使用するを構成することができます。 
  
## <a name="asynchronous-user-defined-functions-udfs"></a>�񓯊��̃��[�U�[��`�֐� (UDF)

�v�Z���ɔ񓯊��� UDF �������ƁA���݂̐����̏�Ԃ��ۑ�����AUDF ���J�n����āA�c��̃Z���̕]�������s����܂��B�v�Z�ł��ׂẴZ���̕]�����I�������Ƃ��ɁA�܂����s���̔񓯊��֐�������ꍇ�AExcel �͔񓯊��֐�����������܂őҋ@���܂��B�e�񓯊��֐������ʂ�񍐂����Ƃ��ɁAExcel �͐�����I�����āA�񓯊��֐��ւ̎Q�Ƃ�܂ރZ����g�p���Ă���Z���̍Čv�Z�̂��߂ɐV�����v�Z�p�X����s���܂��B
  
## <a name="volatile-and-non-volatile-functions"></a>�������֐��Ɣ�������֐�

Excel �ł́A�������֐��̊T�O��T�|�[�g���Ă��܂��B����́A���̊֐��̈������ύX����Ă��Ȃ��Ă� (�֐�����������ꍇ)�A����u�ԂƎ��̏u�Ԃł͒l���قȂ�\��������ƌ��Ȃ����֐��ł��BExcel �́A�Čv�Z�̂��тɁA�������֐����܂܂�Ă���Z������ׂĂ̎Q�Ɛ�Ƌ��ɍĕ]�����܂��B���̂��߁A�������֐��Ɉˑ��������Ă���ƁA�Čv�Z�ɂ����鎞�Ԃ������Ȃ�\��������܂��B�T���߂Ɏg�p����悤�ɂ��Ă��������B
  
���Ɏ��� Excel �֐��͊������ł��B
  
- **NOW**
    
- **TODAY**
    
- **乱数**
    
- **OFFSET**
    
- **INDIRECT**
    
- **INFO** (�����ɂ���ĈقȂ�܂�) 
    
- **CELL** (�����ɂ���ĈقȂ�܂�) 
    
- **SUMIF**(引数によって異なります) 
    
VBA �� C API �́A�������Ƃ��ď�������K�v�̂��郆�[�U�[��`�Ԑ� (UDF) �ɂ��� Excel �ɒʒm�����i��T�|�[�g���Ă��܂��BVBA ��g�p����ꍇ�́A���̂悤�ɂ���� UDF ���������Ƃ��Đ邳��܂��B
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

����ł́AExcel �� VBA �� UDF ���������ł���ƌ��Ȃ��܂��BExcel �́AUDF �̍ŏ��̌Ăяo�����ɁA���� UDF ���������ł��邱�Ƃ�F�����܂��B���̗�̂悤�ɁA������ UDF �͔�������ɖ߂����Ƃ��ł��܂��B
  
C API ��g�p����ꍇ�́AXLL �֐���ŏ��̌Ăяo���O�Ɋ������Ƃ��ēo�^�ł��܂��B�܂��A���[�N�V�[�g�֐��̊�������Ԃ̃I��/�I�t��؂�ւ��邱�Ƃ�ł��܂��B
  
����ł́AExcel �͔͈͈�����󂯎��A�}�N�� �V�[�g�Ɠ����̂�̂Ƃ��Đ錾���ꂽ XLL UDF ��������Ƃ��ď������܂��B���̊���̏�Ԃ́AUDF ���ŏ��ɌĂяo�����Ƃ��� **xlfVolatile** �֐���g�p���邱�ƂŃI�t�ɂł��܂��B 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a>�v�Z���[�h�A�R�}���h�A�I��I�ȍČv�Z�A����уf�[�^ �e�[�u��

Excel �ɂ� 3 �̌v�Z���[�h������܂��B
  
- ����
    
- �e�[�u���ȊO����
    
- �蓮
    
�v�Z�������ɐݒ肳��Ă���ƁA�f�[�^���͂̌�ɍČv�Z��������s����܂��B�܂��A�O�̃Z�N�V�����ŗ��������悤�ɁA����̃C�x���g�̌�ɂ�Čv�Z���������܂��B���ɋ���ȃu�b�N�̏ꍇ�A�Čv�Z�ɒ������Ԃ�������悤�ɂȂ�A���̎��Ԃ����������ꍇ�̓��[�U�[�ɂ�鐧�����K�v�ɂȂ�܂��B�܂�A�Čv�Z�͕K�v�ȂƂ��ɂ̂ݍs���Ƃ������Ƃł��B�����\�ɂ��邽�߂ɁAExcel �ł͎蓮���[�h��T�|�[�g���Ă��܂��B���[�U�[�́AExcel �̃��j���[ �V�X�e�����烂�[�h��I����邱�Ƃ�AVBA�ACOM�A�܂��� C API ��g�p���邱�ƂŁA�v���O�����ɂ���ă��[�h��I����邱�Ƃ�ł��܂��B
  
�f�[�^ �e�[�u���Ƃ́A���[�N�V�[�g��̓���ȍ\���̂��Ƃł��B�ŏ��ɁA���[�U�[�͌��ʂ̌v�Z����[�N�V�[�g�ɃZ�b�g �A�b�v���܂��B����́A1 �܂��� 2 �̃L�[�ɂȂ�ύX�\�ȓ��͂ƁA���̑��̃p�����[�^�[�ɂ���Č��܂�܂��B���ɁA���[�U�[�͈���܂��͗����̃L�[�ɂȂ���͂̒l�̃Z�b�g�ɑ΂��錋�ʂ̃e�[�u����쐬���܂��B�e�[�u���̍쐬�ɂ́A **�f�[�^ �e�[�u�� �E�B�U�[�h**��g�p���܂��B�e�[�u���̃Z�b�g �A�b�v��AExcel �͓��͂� 1 ���v�Z�ɑg�ݍ���ŁA���ʂ̒l��e�[�u���ɃR�s�[���܂��B1 �܂��� 2 �̓��͂��g�p�ł��邽�߁A�f�[�^ �e�[�u���� 1 �����܂��� 2 �����ɂȂ�܂��B 
  
�f�[�^ �e�[�u���̍Čv�Z�̏������@�͎኱�قȂ�܂��B
  
- �Čv�Z�́A�ʏ�̃u�b�N�̍Čv�Z�Ƃ͔񓯊��ɏ�������܂��B����́A����ȃe�[�u���̍Čv�Z�ɂ́A�u�b�N�̎c��̕���������Ԃ������邱�Ƃ����邽�߂ł��B
    
- �z�Q�Ƃ����e����Ă��܂��B���ʂ𓾂邽�߂Ɏg�p�����v�Z���f�[�^ �e�[�u���� 1 �܂��� 2 �̒l�Ɉˑ�����ꍇ�AExcel �͏z�ˑ��̊֌W�Ɋւ���G���[��Ԃ��܂���B 
    
Excel ���f�[�^ �e�[�u���̍Čv�Z��ʂ̕��@�ŏ������邱�ƂƁA���G�Ȍv�Z�܂��͔��ɒ����v�Z�Ɉˑ����鋐��ȃe�[�u���̌v�Z�ɂ͎��Ԃ�������Ƃ�����������AExcel �ł̓f�[�^ �e�[�u���̎����v�Z�𖳌����ł���悤�ɂȂ��Ă��܂��B�����s���ɂ́A�v�Z���[�h�� [�f�[�^ �e�[�u���ȊO����] �ɐݒ肵�܂��B�v�Z�����̃��[�h�̂Ƃ��ɂ́A���[�U�[�� F9 ��������A����Ɠ����̃v���O�����ɂ�鑀�����s���邱�ƂŁA�f�[�^ �e�[�u�����Čv�Z����܂��B
  
Excel �́A�Čv�Z���[�h�̕ύX�ƍČv�Z�̐���ɗ��p�ł��郁�\�b�h����J���Ă��܂��B����ɊY�����郁�\�b�h�́A�o�[�W�������i�ނ��Ƃɉ��P����Ă��āA���ׂ������䂪�\�ɂȂ��Ă��܂��B����Ɋ֘A���� C API �̋@�\�́AExcel �o�[�W���� 5 �Ŏg�p�\��������̂𔽉f���Ă��邽�߁A�������V���� VBA ��g�p���邱�Ƃœ������̂Ɠ�������͓����܂���B 
  
Excel ���蓮�v�Z���[�h�̂Ƃ��ɍł�p�ɂɎg�p����郁�\�b�h�́A�u�b�N�A���[�N�V�[�g�A����є͈͂̑I��I�Ȍv�Z��\�ɂ��郁�\�b�h�A�J���Ă��邷�ׂẴu�b�N�̊��S�ȍČv�Z��\�ɂ��郁�\�b�h�A����Ɉˑ��֌W�c���[�ƌv�Z�`�F�[���̊��S�ȍč\�z��\�ɂ��郁�\�b�h�ł��B
  
### <a name="range-calculation"></a>�͈͌v�Z

�L�[�{�[�h����: �Ȃ�
  
VBA: **Range.Calculate** (Excel 2000 �œ�������AExcel 2007 �ŕύX����Ă��܂�) ����� **Range.CalculateRowMajorOrder** (Excel 2007 �œ�������܂���) 
  
C API: �T�|�[�g�Ȃ�
  
- **[�蓮] ���[�h**
    
    ����͈͓̔�̃Z���݂̂�Čv�Z���܂� (�Z�����_�[�e�B���ǂ����͊֌W����܂���)�B **Range.Calculate** ���\�b�h�̓���� Excel 2007 �ŕύX����Ă��܂��B�������A�ȑO�̓���� **Range.CalculateRowMajorOrder** ���\�b�h�ŃT�|�[�g����Ă��܂��B 
    
- **[����] �܂��� [�e�[�u���ȊO����] ���[�h**
    
    �u�b�N��Čv�Z���܂����A�͈͂̍Čv�Z�܂��͔͈͂Ɋ܂܂��Z���̍Čv�Z��������܂���B
    
### <a name="active-worksheet-calculation"></a>�A�N�e�B�u�ȃ��[�N�V�[�g�̌v�Z

�L�[�{�[�h����: SHIFT + F9
  
VBA: **ActiveSheet.Calculate**
  
C API: **xlcCalculateDocument**
  
- **���ׂẴ��[�h**
    
    �A�N�e�B�u�ȃ��[�N�V�[�g��ł̂݁A�v�Z�̃}�[�N���t�����Ă���Z����Čv�Z���܂��B
    
### <a name="specified-worksheet-calculation"></a>�w�肳�ꂽ���[�N�V�[�g�̌v�Z

�L�[�{�[�h����: �Ȃ�
  
VBA: **Worksheets(** �Q�� **).Calculate**
  
C API: �T�|�[�g�Ȃ�
  
- **���ׂẴ��[�h**
    
    �w�肳�ꂽ���[�N�V�[�g��ł̂݁A�_�[�e�B�ȃZ���Ƃ��̃Z���̎Q�Ɛ��Čv�Z���܂��B�Q�Ƃ͕�����Ƃ��Ẵ��[�N�V�[�g�̖��O�A�܂��͊֘A����u�b�N�̃C���f�b�N�X�ԍ��ł��B
    
    Excel 2000 �ȍ~�̃o�[�W�����ł́A **Boolean** ���[�N�V�[�g �v���p�e�B�� **EnableCalculation** �v���p�e�B�����J����Ă��܂��B����� **False** ���� **True** �ɐݒ肷��ƁA�w�肳�ꂽ���[�N�V�[�g��̂��ׂẴZ�����_�[�e�B�ɂȂ�܂��B�������[�h�̏ꍇ�́A����ɂ��u�b�N�S�̂̍Čv�Z��g���K�[����܂��B 
    
    �蓮���[�h�̏ꍇ�́A���̃R�[�h�ŃA�N�e�B�u �V�[�g�݂̂̍Čv�Z���s���܂��B
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a>�u�b�N�̃c���[�̍č\�z�ƍČv�Z�̋���

�L�[�{�[�h����: CTRL + ALT + SHIFT + F9 (Excel 2002 �œ�������܂���)
  
VBA: **Workbooks(** �Q�� **).ForceFullCalculation** (Excel 2007 �œ�������܂���) 
  
C API: �T�|�[�g�Ȃ�
  
- **���ׂẴ��[�h**
    
    Excel �ɂ���ē���̃u�b�N�̈ˑ��֌W�c���[�ƌv�Z�`�F�[�����č\�z����A������܂�ł��邷�ׂẴZ���̍Čv�Z��������܂��B
    
### <a name="all-open-workbooks"></a>�J���Ă��邷�ׂẴu�b�N

�L�[�{�[�h����: F9
  
VBA: **Application.Calculate**
  
C API: **xlcCalculateNow**
  
- **���ׂẴ��[�h**
    
    Excel によってダーティのマークが付けられたすべてのセル (揮発性データと変更されたデータの参照先、およびプログラムによりダーティのマークが付けられたセル) を再計算します。計算モードが [テーブル以外自動] の場合は、更新を必要とするテーブルに加えて、すべての揮発性関数とその関数の参照先も生産します。
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a>�J���Ă��邷�ׂẴu�b�N�̃c���[�̍č\�z�ƌv�Z�̋���

�L�[�{�[�h����: CTRL + ALT + F9
  
VBA: **Application.CalculateFull**
  
C API: �T�|�[�g�Ȃ�
  
- **���ׂẴ��[�h**
    
    �J���Ă��邷�ׂẴu�b�N�Ɋ܂܂�邷�ׂẴZ����Čv�Z���܂��B�v�Z���[�h�� [�e�[�u���ȊO����] �̏ꍇ�́A�e�[�u���̍Čv�Z��������܂��B
    
## <a name="see-also"></a>�֘A����



[Excel �ł̃}���`�X���b�h�Čv�Z](multithreaded-recalculation-in-excel.md)
  
[Excel �Ŏg�p�����f�[�^�^](data-types-used-by-excel.md)
  
[Excel �̃������Ǘ�](memory-management-in-excel.md)
  
[Excel �v���O���~���O�̊T�O](excel-programming-concepts.md)

