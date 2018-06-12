---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- xlrunningoncluster
localization_priority: Normal
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: f42ccbeb94e1fc6b6cf880f1b32ee1bfeb24997e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799009"
---
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
���[�U�[��`�֐����N���X�^�[�Ŏ��s����Ă��邩�ǂ���������l��Ԃ��܂��B 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>�p�����[�^�[

���̊֐��ɂ͈����͂���܂���B
  
## <a name="return-value"></a>�߂�l

�֐��� Excel �v���Z�X�Ŏ��s����Ă���ꍇ�A **xlTypeInt** �^�� **XLOPER12** �� 0 ��Ԃ��܂��B�֐����N���X�^�[��Ŏ��s���Ă���ꍇ�A�߂�l�̌^�ƒl�́A�N���X�^�[ �R�l�N�^ �v���o�C�_�[�ɂ���Č��܂�܂��B
  
## <a name="requirements"></a>�v��

���̊֐��́AXlcall.h �w�b�_�[ �t�@�C���Œ�`����܂��B
  
## <a name="see-also"></a>�֘A����

- [�N���X�^�[ �Z�[�t�֐�](cluster-safe-functions.md)
- [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

