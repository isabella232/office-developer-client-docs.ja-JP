---
title: IMAPIFormContainerGetDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 994041d050df56fd3fa3c0e599542e05a202ad65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416133"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="5ab2c-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="5ab2c-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="5ab2c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ab2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ab2c-105">フォームコンテナーの表示名を返します。</span><span class="sxs-lookup"><span data-stu-id="5ab2c-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="5ab2c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5ab2c-106">Parameters</span></span>

 <span data-ttu-id="5ab2c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5ab2c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5ab2c-108">順番返される文字列の型を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="5ab2c-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="5ab2c-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5ab2c-109">The following flag can be set:</span></span>
    
<span data-ttu-id="5ab2c-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5ab2c-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5ab2c-111">返される文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="5ab2c-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="5ab2c-112">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="5ab2c-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="5ab2c-113">_pszdisplayname_</span><span class="sxs-lookup"><span data-stu-id="5ab2c-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="5ab2c-114">読み上げフォームコンテナーの表示名を含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5ab2c-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5ab2c-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="5ab2c-115">Return value</span></span>

<span data-ttu-id="5ab2c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ab2c-116">S_OK</span></span> 
  
> <span data-ttu-id="5ab2c-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="5ab2c-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="5ab2c-118">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="5ab2c-118">MFCMAPI reference</span></span>

<span data-ttu-id="5ab2c-119">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ab2c-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5ab2c-120">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="5ab2c-120">**File**</span></span>|<span data-ttu-id="5ab2c-121">**関数**</span><span class="sxs-lookup"><span data-stu-id="5ab2c-121">**Function**</span></span>|<span data-ttu-id="5ab2c-122">**コメント**</span><span class="sxs-lookup"><span data-stu-id="5ab2c-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5ab2c-123">FormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="5ab2c-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="5ab2c-124">CFormContainerDlg:: CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="5ab2c-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="5ab2c-125">mfcmapi は、 **imapiformcontainer:: getdisplay**メソッドを使用して、CFormContainerDlg をレンダリングするときにフォームコンテナーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="5ab2c-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5ab2c-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ab2c-126">See also</span></span>



[<span data-ttu-id="5ab2c-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5ab2c-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


<span data-ttu-id="5ab2c-128">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="5ab2c-128">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

