---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798761"
---
# <a name="calludf"></a><span data-ttu-id="46087-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="46087-103">CallUDF</span></span>

<span data-ttu-id="46087-104">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="46087-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="46087-105">���p�t�H�[�}���X�̃R���s���[�e�B���O���Ń��[�U�[��\`�֐���Ăяo���܂��B</span><span class="sxs-lookup"><span data-stu-id="46087-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="46087-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="46087-106">Parameters</span></span>

<span data-ttu-id="46087-107">_セッション Id_</span><span class="sxs-lookup"><span data-stu-id="46087-107">_SessionId_</span></span>
  
> <span data-ttu-id="46087-108">�Ăяo����s���Z�b�V������ ID�B</span><span class="sxs-lookup"><span data-stu-id="46087-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="46087-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="46087-109">_XLLName_</span></span>
  
> <span data-ttu-id="46087-110">���[�U�[��\`�֐����܂܂�� XLL �̖��O�B</span><span class="sxs-lookup"><span data-stu-id="46087-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="46087-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="46087-111">_UDFName_</span></span>
  
> <span data-ttu-id="46087-112">���[�U�[��\`�֐��̖��O�B</span><span class="sxs-lookup"><span data-stu-id="46087-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="46087-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="46087-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="46087-114">���[�U�[��\`�֐����I������Ƃ��ɃR�l�N�^���Ăяo���K�v������֐��B</span><span class="sxs-lookup"><span data-stu-id="46087-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="46087-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="46087-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="46087-p101">Excel �ƃR�l�N�^���A�ۗ����̃��[�U�[��\`�֐��̌Ăяo����ǐՂ��邽�߂Ɏg�p����񓯊��n���h���B�R�l�N�^�ɂ���āA��قǁA�Ăяo�����I�������Ƃ� ( _CallBackAddr_ �����ɓn���ꂽ�֐��|�C���^�[��g�p���� Excel �ɃR�[���o�b�N����Ƃ�) �Ɏg�p����܂��B</span><span class="sxs-lookup"><span data-stu-id="46087-p101">The asynchronous handle used by Excel and the connector to track the pending user-defined function call. The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="46087-118">_について_</span><span class="sxs-lookup"><span data-stu-id="46087-118">_ArgCount_</span></span>
  
> <span data-ttu-id="46087-p102">���[�U�[��\`�֐��ɓn���������̐��B�ő�l�� 255 �ł��B</span><span class="sxs-lookup"><span data-stu-id="46087-p102">The number of arguments to pass to the user-defined function. The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="46087-121">_パラメーター 1_</span><span class="sxs-lookup"><span data-stu-id="46087-121">_Parameter1_</span></span>
  
> <span data-ttu-id="46087-p103">���[�U�[��\`�֐��ɓn���l�B _ArgCount_ �Ŏ�����Ă���p�����[�^�[���Ƃɂ��̈����𔽕����܂��B</span><span class="sxs-lookup"><span data-stu-id="46087-p103">A value to pass to the user-defined function. Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="46087-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="46087-124">Return value</span></span>

<span data-ttu-id="46087-125">UDF �Ăяo��������ɊJ�n���ꂽ�ꍇ�ɂ� **xlHpcRetSuccess**�B **SessionId** �����������ȏꍇ�ɂ� _xlHpcRetInvalidSessionId_�B�^�C���A�E�g�ȂǑ��̃G���[���������ꍇ�ɂ� **xlHpcRetCallFailed**�B�Ăяo���ɂ���ăG���[ �R�[�h ( **xlHpcRetSuccess** �ȊO) ���Ԃ����ꍇ�AExcel �� UDF �Ăяo�������s�����ƌ��Ȃ��A  _pxAsyncHandle_ ��s�킸�ɁA�R�[���o�b�N�̔�����z�肵�܂���B</span><span class="sxs-lookup"><span data-stu-id="46087-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46087-126">����</span><span class="sxs-lookup"><span data-stu-id="46087-126">Remarks</span></span>

<span data-ttu-id="46087-127">���̊֐��͔񓯊��Ŏ��s����܂��B</span><span class="sxs-lookup"><span data-stu-id="46087-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="46087-128">�֘A����</span><span class="sxs-lookup"><span data-stu-id="46087-128">See also</span></span>

- <span data-ttu-id="46087-129">[Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)</span><span class="sxs-lookup"><span data-stu-id="46087-129">[Excel Cluster Connector Functions](excel-cluster-connector-functions.md)</span></span>

