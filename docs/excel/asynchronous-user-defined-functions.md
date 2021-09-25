---
title: 非同期のユーザー定義関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 142eb27e-fb6f-4da3-bfb7-a88115bbb5d5
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab505a5f929ecc258d39abea6ff9553998bb6b01
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614627"
---
# <a name="asynchronous-user-defined-functions"></a>非同期のユーザー定義関数

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 can call user-defined functions asynchronously. Calling functions asynchronously can improve performance by allowing several calculations to run at the same time. When you run user-defined functions on a compute cluster, calling functions asynchronously enables several computers to be used to complete the calculations.
  
## <a name="when-to-use-asynchronous-user-defined-functions"></a>非同期ユーザー定義関数を使用する場合

Some user-defined functions must wait for external resources. While they wait, the Excel calculation thread is blocked. In Excel 2013, user-defined functions can run asynchronously. This frees the calculation thread to run other calculations while the user-defined function waits.
  
In Excel 2007, programmers could run multiple user-defined functions at the same time by increasing the number of threads used in multiple-thread recalculations. This method has drawbacks primarily because the number of threads is a setting scoped to an application and cannot be controlled at the level of a single function or an add-in.
  
�֐����O�����\�[�X��҂K�v������ꍇ�A�v���O���}�[�͔񓯊��̃��[�U�[��`�֐��̌Ăяo����g�p����K�v������܂��B���Ƃ��΁A�C���^�[�l�b�g��� SOAP �v���𑗐M����֐��́A�l�b�g���[�N�ŗv�����z�M����A�����[�g �T�[�o�[�ŗv�����������A�l�b�g���[�N�Ō��ʂ��Ԃ����̂�҂K�v������܂��B���̏ꍇ�A�d�v�ȃR���s���[�e�B���O�͔��������AExcel �ő��̌v�Z��p�����čs�����Ƃ��ł��܂��B
  
�֐����v�Z�N���X�^�[�ɗv���𑗐M���Ă���ꍇ�A�v���O���}�[�͔񓯊��̃��[�U�[��`�֐���g�p���邱�Ƃ�ł��܂��B���̏ꍇ�A�l�b�g���[�N�̒x����҂����łȂ��A�N���X�^�[�͌X�̌Ăяo����ʁX�̃T�[�o�[�Ŏ��s�ł��܂��B�X�̌Ăяo������������܂ő҂��Ȃ����Ƃɂ��A�Ăяo����d�����邱�Ƃ��ł��邽�߃p�t�H�[�}���X�����P���܂��B�ꍇ�ɂ���ẮA�啝�ɉ��P���܂��B
  
> [!NOTE]
> [!����] ���[�U�[��`�֐��́A�񓯊��ƃN���X�^�[ �Z�[�t�̗����Ƃ��ēo�^���邱�Ƃ͂ł��܂���B 
  
## <a name="writing-an-asynchronous-user-defined-function"></a>非同期ユーザー定義関数の作成

Asynchronous user-defined functions must keep track of a handle and use that handle when informing Excel that the function call is finished. An asynchronous user-defined function is split into two pieces. The first piece is the standard UDF entry point, which will launch a second, separate asynchronous operation. Callbacks into Excel should be made during the UDF entry point. The first launching portion of the function will then return control of its calculation thread to Excel, which will continue calculation. When the second asynchronous operation is complete, it must call back into Excel and provide Excel with its result. 
  
> [!NOTE]
> [!����] �񓯊������ŕK�v�� UDF �ɓn���ꂽ���ׂĂ̈����ɂ��ẮAUDF �G���g�� �|�C���g���Ԃ��ꂽ�Ƃ��� Excel �������̈����������邽�߁A�֐��̏ڍׂ��R�s�[����Ȃ���΂Ȃ�܂���B 
  
Excel �ł́A�񓯊��� UDF �Ăяo���̃��C�t �T�C�N����Ǘ����邽�߁AXLL �A�h�C�����g�����Ƃ̂ł���C�x���g�̃Z�b�g���񋟂���܂��B�����̃C�x���g�́AExcel �ł̌v�Z�������������A�v�Z���������ꂽ��������܂��B
  
### <a name="declaring-an-asynchronous-function"></a>非同期関数の宣言

�񓯊��̃��[�U�[��`�֐��̓o�^���ɁA�����񓯊��Ƃ��Đ錾����K�v������܂��B����́AXLOPER12 �\�� (�o�^�^�C�v�̕������ "X" �ƕ\�������) ��|�C���g����p�����[�^�[�� UDF �p�����[�^�[�̈ꗗ�̔C�ӂ̏ꏊ�ɒǉ����邱�Ƃɂ���Ď��s����܂��BExcel �ł́A���̃p�����[�^�[��g�p���Ĕ񓯊��̌Ăяo���n���h����n���܂��BXLL �A�h�C���́A�񓯊��̌Ăяo���n���h���ƁA�֐��̌��ʂ̏������ł����炻�̌��ʂ� Excel �ɓn���K�v������܂��B����ɁAUDF �̖߂�l�̌^�́A������^�̍ŏ��̕����Ƃ��� ">" �ɂ���Ďw�肳��� **void** �łȂ���΂Ȃ�܂���BUDF �̓��������� Excel �ɒl��Ԃ��Ȃ����߁A�߂�l�̌^�� void �ł��B����ɁAXLL �A�h�C�����R�[���o�b�N�ɂ���Ēl��񓯊��ŕԂ��܂��B 
  
�񓯊��̊֐���X���b�h �Z�[�t�Ƃ��Đ錾����ƁAUDF �̓����������}���`�X���b�h�̍Čv�Z�Ŏg�p����܂��B 
  
���̃R�[�h��́A"\>QX" ��o�^�^�C�v�̕�����Ƃ��Ďg�p���ēo�^���ꂽ�񓯊��̃��[�U�[��`�֐�������܂��B
  
```cpp
void MyAsyncUDF(LPXLOPER12 arg1, LPXLOPER12 pxAsyncHandle)
{
…
}
```

### <a name="returning-values"></a>値を返す

�񓯊��̌Ăяo���̌��ʂ̏������ł�����A�^ [xlAsyncReturn](xlasyncreturn.md) �̃R�[���o�b�N����s���邱�Ƃɂ���� XLL �A�h�C���͂��̌��ʂ� Excel �ɕԂ��܂��B
  
**xlAsyncReturn** �́A�Čv�Z���Ɍv�Z�ȊO�̃X���b�h�Ɏg�p�ł���B��̃R�[���o�b�N�ł��B���������āA�񓯊��� UDF �̔񓯊������ő��̃R�[���o�b�N�͎��s���Ȃ��ł��������B 
  
### <a name="handling-events"></a>イベントを処理する

Excel 2010 �ȍ~�AXLL �͔񓯊��֐��̃��C�t �T�C�N����Ǘ����邽�߂ɐ݌v���ꂽ�C�x���g���M�ł��܂��B�ڂ����́A�u[�C�x���g�̏���](handling-events.md)�v��������������B
  
## <a name="see-also"></a>関連項目

- [Excel XLL の開発](developing-excel-xlls.md)

