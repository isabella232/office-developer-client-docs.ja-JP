---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798938"
---
# <a name="opensession"></a><span data-ttu-id="6cec0-103">OpenSession</span><span class="sxs-lookup"><span data-stu-id="6cec0-103">OpenSession</span></span>

<span data-ttu-id="6cec0-104">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6cec0-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6cec0-105">���[�U�[��\`�֐�����s�ł���Z�b�V������쐬���܂��B</span><span class="sxs-lookup"><span data-stu-id="6cec0-105">Creates a session in which user-defined functions can be executed.</span></span>
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a><span data-ttu-id="6cec0-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="6cec0-106">Parameters</span></span>

<span data-ttu-id="6cec0-107">_Params_</span><span class="sxs-lookup"><span data-stu-id="6cec0-107">_Params_</span></span>
  
> <span data-ttu-id="6cec0-p101">�Z�b�V�����̃p�����[�^�[�́A�Z�~�R�����ŋ�؂�ꂽ UNICODE ������ւ̃|�C���^�[�BExcel �ł́A���̈����͎g�p���܂���B</span><span class="sxs-lookup"><span data-stu-id="6cec0-p101">A pointer to semicolon-delimited UNICODE string of parameters for the session. Excel does not use this argument.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6cec0-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6cec0-110">Return value</span></span>

<span data-ttu-id="6cec0-111">�Z�b�V����������ɍ쐬���ꂽ�ꍇ�́A���̃N���X�^�[ �R�l�N�^�ɑ΂��鑼�̌Ăяo���Ŏg�p����Z�b�V���� ID�B����ȊO�̏ꍇ�� **xlHpcRetCallFailed**�B</span><span class="sxs-lookup"><span data-stu-id="6cec0-111">A session ID to use in other calls to the cluster connector, if the session was successfully created; otherwise **xlHpcRetCallFailed**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6cec0-112">�֘A����</span><span class="sxs-lookup"><span data-stu-id="6cec0-112">See also</span></span>

- <span data-ttu-id="6cec0-113">[Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)</span><span class="sxs-lookup"><span data-stu-id="6cec0-113">[Excel Cluster Connector Functions](excel-cluster-connector-functions.md)</span></span>

