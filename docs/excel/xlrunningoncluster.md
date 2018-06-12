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
# <a name="xlrunningoncluster"></a><span data-ttu-id="8288d-104">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="8288d-104">xlRunningOnCluster</span></span>

<span data-ttu-id="8288d-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8288d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8288d-106">���[�U�[��\`�֐����N���X�^�[�Ŏ��s����Ă��邩�ǂ���������l��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="8288d-106">Returns a value that indicates whether the user-defined function is running on a cluster.</span></span> 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="8288d-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="8288d-107">Parameters</span></span>

<span data-ttu-id="8288d-108">���̊֐��ɂ͈����͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="8288d-108">This function has no arguments.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="8288d-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="8288d-109">Return value</span></span>

<span data-ttu-id="8288d-p101">�֐��� Excel �v���Z�X�Ŏ��s����Ă���ꍇ�A **xlTypeInt** �^�� **XLOPER12** �� 0 ��Ԃ��܂��B�֐����N���X�^�[��Ŏ��s���Ă���ꍇ�A�߂�l�̌^�ƒl�́A�N���X�^�[ �R�l�N�^ �v���o�C�_�[�ɂ���Č��܂�܂��B</span><span class="sxs-lookup"><span data-stu-id="8288d-p101">If the function is running in an Excel process, returns 0 in an **XLOPER12** of type **xlTypeInt**. If the function is running on a cluster, the return type and value is determined by the cluster connector provider.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="8288d-112">�v��</span><span class="sxs-lookup"><span data-stu-id="8288d-112">Requirements</span></span>

<span data-ttu-id="8288d-113">���̊֐��́AXlcall.h �w�b�_�[ �t�@�C���Œ�\`����܂��B</span><span class="sxs-lookup"><span data-stu-id="8288d-113">This function is defined in the Xlcall.h header file.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8288d-114">�֘A����</span><span class="sxs-lookup"><span data-stu-id="8288d-114">See also</span></span>

- <span data-ttu-id="8288d-115">[�N���X�^�[ �Z�[�t�֐�](cluster-safe-functions.md)</span><span class="sxs-lookup"><span data-stu-id="8288d-115">[Cluster Safe Functions](cluster-safe-functions.md)</span></span>
- [<span data-ttu-id="8288d-116">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="8288d-116">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

