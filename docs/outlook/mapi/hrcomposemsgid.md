---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c035780d3d790d94551860a418401e63da1c2151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348049"
---
# <a name="hrcomposemsgid"></a><span data-ttu-id="88b49-103">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="88b49-103">HrComposeMsgID</span></span>

  
  
<span data-ttu-id="88b49-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88b49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88b49-105">オブジェクトの複合エントリ識別子 (通常はメッセージストア内のメッセージ) を表す ASCII 文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="88b49-105">Creates an ASCII string representing a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="88b49-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="88b49-106">Header file:</span></span>  <br/> |<span data-ttu-id="88b49-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="88b49-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="88b49-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="88b49-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="88b49-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="88b49-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="88b49-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="88b49-110">Called by:</span></span>  <br/> |<span data-ttu-id="88b49-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="88b49-111">Client applications</span></span>  <br/> |
   
```cpp
HrComposeMsgID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  LPSTR FAR * pszMsgID
);
```

## <a name="parameters"></a><span data-ttu-id="88b49-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="88b49-112">Parameters</span></span>

 <span data-ttu-id="88b49-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="88b49-113">_psession_</span></span>
  
> <span data-ttu-id="88b49-114">順番クライアントアプリケーションによって使用されているセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="88b49-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="88b49-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="88b49-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="88b49-116">順番メッセージまたはその他のオブジェクトを含むメッセージストアのレコードキーのサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="88b49-116">[in] Size, in bytes, of the record key of the message store that contains the message or other object.</span></span> <span data-ttu-id="88b49-117">_cbStoreRecordKey_パラメーターに0が渡された場合、 _pszMsgID_パラメーターは、テキストに変換されたエントリ id のコピーを指します。</span><span class="sxs-lookup"><span data-stu-id="88b49-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _pszMsgID_ parameter points to a copy of the entry identifier converted to text.</span></span> 
    
 <span data-ttu-id="88b49-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="88b49-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="88b49-119">順番メッセージまたはその他のオブジェクトを含むメッセージストアの record キーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="88b49-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="88b49-120">_cbmsgeid_</span><span class="sxs-lookup"><span data-stu-id="88b49-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="88b49-121">順番メッセージまたはその他のオブジェクトのエントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="88b49-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="88b49-122">_pmsgeid_</span><span class="sxs-lookup"><span data-stu-id="88b49-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="88b49-123">順番オブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="88b49-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="88b49-124">_pszMsgID_</span><span class="sxs-lookup"><span data-stu-id="88b49-124">_pszMsgID_</span></span>
  
> <span data-ttu-id="88b49-125">読み上げ返された ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="88b49-125">[out] Pointer to the returned ASCII string.</span></span> <span data-ttu-id="88b49-126">_cbStoreRecordKey_パラメーターが0より大きい場合、 _pszMsgID_パラメーターは、テキストに変換された複合エントリ識別子を指します。</span><span class="sxs-lookup"><span data-stu-id="88b49-126">If the  _cbStoreRecordKey_ parameter is greater than zero, the  _pszMsgID_ parameter points to a compound entry identifier converted to text.</span></span> <span data-ttu-id="88b49-127">_cbStoreRecordKey_が0の場合、 _pszMsgID_は、テキストに変換された非複合エントリ識別子を指します。</span><span class="sxs-lookup"><span data-stu-id="88b49-127">If  _cbStoreRecordKey_ is zero,  _pszMsgID_ points to a noncompound entry identifier converted to text.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="88b49-128">Return value</span><span class="sxs-lookup"><span data-stu-id="88b49-128">Return value</span></span>

<span data-ttu-id="88b49-129">なし。</span><span class="sxs-lookup"><span data-stu-id="88b49-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88b49-130">解説</span><span class="sxs-lookup"><span data-stu-id="88b49-130">Remarks</span></span>

<span data-ttu-id="88b49-131">複合エントリ識別子が作成されているメッセージまたはその他のオブジェクトがメッセージストアに存在する場合、識別子文字列は、オブジェクトのエントリ識別子とストアの record キーから作成されます。</span><span class="sxs-lookup"><span data-stu-id="88b49-131">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier string is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="88b49-132">オブジェクトがストアに存在しない場合、つまり、 _cbStoreRecordKey_パラメーターで渡されたストアレコードキーのバイト数が0の場合、オブジェクトのエントリ識別子は単にコピーされ、文字列に変換されます。</span><span class="sxs-lookup"><span data-stu-id="88b49-132">If the object is not in a store, that is, if the byte count for the store record key passed in the  _cbStoreRecordKey_ parameter is zero, the object's entry identifier is simply copied and converted into a string.</span></span> 
  
<span data-ttu-id="88b49-133">**HrComposeMsgID**関数の呼び出しは、hr の[id](hrcomposeeid.md)関数を呼び出し、次に[hrszfromentryid](hrszfromentryid.md)関数を呼び出すことと同じです。</span><span class="sxs-lookup"><span data-stu-id="88b49-133">Calling the **HrComposeMsgID** function is equivalent to calling the [HrComposeEID](hrcomposeeid.md) function and then the [HrSzFromEntryID](hrszfromentryid.md) function.</span></span> 
  
 <span data-ttu-id="88b49-134">**HrComposeMsgID**では、クライアントアプリケーションが複合エントリ識別子を使用して、複数のストア内のオブジェクトを操作することができます。</span><span class="sxs-lookup"><span data-stu-id="88b49-134">**HrComposeMsgID** enables client applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="88b49-135">アプリケーションは[HrDecomposeMsgID](hrdecomposemsgid.md)関数を呼び出して、複合エントリ識別子を元の constituents に分割できます。</span><span class="sxs-lookup"><span data-stu-id="88b49-135">An application can call the [HrDecomposeMsgID](hrdecomposemsgid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  

