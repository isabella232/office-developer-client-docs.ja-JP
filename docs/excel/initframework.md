---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- initframework function [excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 2d7e3286d794d6f21da9ef83ca44d18ec242c063
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798879"
---
# <a name="initframework"></a>InitFramework

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�t���[�����[�N ���C�u���������������t���[�����[�N ���C�u�����֐��B����͒P�ɁA���Ɋ��蓖�Ă��Ă��郁�����������āA�ꎞ�I�� **XLOPER**/ **XLOPER12** ������ �f�[�^�\������������܂��B 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a>�p�����[�^�[

���̊֐��Ɉ����͂���܂���B
  
## <a name="return-value"></a>�߂�l

���̊֐��͒l��Ԃ��܂���B
  
## <a name="example"></a>��

���̗�ł� **InitFramework** �֐���g�p���āA���ׂĂ̈ꎞ�������������܂��B 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a>�֘A����



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

