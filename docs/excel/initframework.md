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
# <a name="initframework"></a><span data-ttu-id="c7ff1-104">InitFramework</span><span class="sxs-lookup"><span data-stu-id="c7ff1-104">InitFramework</span></span>

 <span data-ttu-id="c7ff1-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c7ff1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c7ff1-106">�t���[�����[�N ���C�u���������������t���[�����[�N ���C�u�����֐��B����͒P�ɁA���Ɋ��蓖�Ă��Ă��郁�����������āA�ꎞ�I�� **XLOPER**/ **XLOPER12** ������ �f�[�^�\������������܂��B</span><span class="sxs-lookup"><span data-stu-id="c7ff1-106">Framework library function that initializes the Framework library, which simply initializes the temporary **XLOPER**/ **XLOPER12** memory data structures, freeing any memory that has already been allocated.</span></span> 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a><span data-ttu-id="c7ff1-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="c7ff1-107">Parameters</span></span>

<span data-ttu-id="c7ff1-108">���̊֐��Ɉ����͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="c7ff1-108">This function takes no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="c7ff1-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c7ff1-109">Return value</span></span>

<span data-ttu-id="c7ff1-110">���̊֐��͒l��Ԃ��܂���B</span><span class="sxs-lookup"><span data-stu-id="c7ff1-110">This function does not return a value.</span></span>
  
## <a name="example"></a><span data-ttu-id="c7ff1-111">��</span><span class="sxs-lookup"><span data-stu-id="c7ff1-111">Example</span></span>

<span data-ttu-id="c7ff1-112">���̗�ł� **InitFramework** �֐���g�p���āA���ׂĂ̈ꎞ�������������܂��B</span><span class="sxs-lookup"><span data-stu-id="c7ff1-112">This example uses the **InitFramework** function to free all temporary memory.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="c7ff1-113">�֘A����</span><span class="sxs-lookup"><span data-stu-id="c7ff1-113">See also</span></span>



<span data-ttu-id="c7ff1-114">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="c7ff1-114">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

