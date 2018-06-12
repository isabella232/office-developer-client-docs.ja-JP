---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- xlgetbinaryname function [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798978"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
[XlDefineBinaryName 関数](xldefinebinaryname.md)によって保存されたデータへのハンドルを返すために使用します。 定義されているバイナリの名前を使用してデータはブックと共に保存され、名前でいつでもアクセスできます。 詳細については、 [Excel の XLL の開発での既知の問題](known-issues-in-excel-xll-development.md)で「バイナリの名前スコープの制限」を参照してください。
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>�p�����[�^�[

_pxRes_(**xltypeBigData**または**xltypeErr**)
  
�擾���ꂽ�f�[�^�܂��̓G���[��w�肷�� Bigdata �\���̂́A�擾�ł��Ȃ������f�[�^�܂��͒�`����Ă��Ȃ����O�ɂȂ�܂��B�֐����Ԃ����ƁA **XLOPER******/  �� **hdata** �����o�[�ɂ́A���O�t���f�[�^�̃n���h�����܂܂�܂��B  _pxRes_ ���s�v�ɂȂ�ꍇ�A **xlFree** �ւ̌Ăяo���ŉ�����Ȃ���΂Ȃ�܂���B 
  
_pxName_(**xltypeStr**)
  
�f�[�^�̖��O��w�肷�镶����B
  
## <a name="remarks"></a>����

Microsoft Excel �ɂ́A **hdata** �ŕԂ���郁���� �n���h��������܂��BWindows �ł́A�n���h���̓O���[�o�� ������ �n���h���ł� ( **GlobalAlloc** �֐��Ŋ��蓖�Ă��܂�)�B 
  
## <a name="see-also"></a>�֘A����

- [xlDefineBinaryName](xldefinebinaryname.md)
- [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

