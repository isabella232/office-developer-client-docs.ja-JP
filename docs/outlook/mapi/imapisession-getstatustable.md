---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407138"
---
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="099d6-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="099d6-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="099d6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="099d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="099d6-105">セッション内のすべての MAPI リソースに関する情報を含むテーブルである状態テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="099d6-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="099d6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="099d6-106">Parameters</span></span>

 <span data-ttu-id="099d6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="099d6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="099d6-108">[in]文字列である列の形式を決定するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="099d6-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="099d6-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="099d6-109">The following flag can be set:</span></span>
    
<span data-ttu-id="099d6-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="099d6-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="099d6-111">文字列列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="099d6-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="099d6-112">このフラグMAPI_UNICODE設定されていない場合、文字列列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="099d6-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="099d6-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="099d6-113">_lppTable_</span></span>
  
> <span data-ttu-id="099d6-114">[out]状態テーブルへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="099d6-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="099d6-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="099d6-115">Return value</span></span>

<span data-ttu-id="099d6-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="099d6-116">S_OK</span></span> 
  
> <span data-ttu-id="099d6-117">テーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="099d6-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="099d6-118">注釈</span><span class="sxs-lookup"><span data-stu-id="099d6-118">Remarks</span></span>

<span data-ttu-id="099d6-119">**IMAPISession::GetStatusTable** メソッドは、セッション内のすべての MAPI リソースに関する情報を含む状態テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="099d6-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="099d6-120">表には、MAPI サブシステムに関する情報を示す 1 行、MAPI スプーラー用の 1 行、統合アドレス帳用の 1 行、プロファイル内のサービス プロバイダーごとに 1 行があります。</span><span class="sxs-lookup"><span data-stu-id="099d6-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="099d6-121">状態テーブルの必須列と省略可能列の完全な一覧については、「Status [Tables」を参照してください](status-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="099d6-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="099d6-122">_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると [、IMAPITable::QueryColumns](imapitable-querycolumns.md)および [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="099d6-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="099d6-123">このフラグは [、IMAPITable::QuerySortOrder](imapitable-querysortorder.md) メソッドによって返される並べ替え順序のプロパティの種類も制御します。</span><span class="sxs-lookup"><span data-stu-id="099d6-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="099d6-124">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="099d6-124">MFCMAPI reference</span></span>

<span data-ttu-id="099d6-125">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="099d6-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="099d6-126">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="099d6-126">**File**</span></span>|<span data-ttu-id="099d6-127">**関数**</span><span class="sxs-lookup"><span data-stu-id="099d6-127">**Function**</span></span>|<span data-ttu-id="099d6-128">**コメント**</span><span class="sxs-lookup"><span data-stu-id="099d6-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="099d6-129">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="099d6-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="099d6-130">CMainDlg::OnStatusTable</span><span class="sxs-lookup"><span data-stu-id="099d6-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="099d6-131">MFCMAPI は **IMAPISession::GetStatusTable** メソッドを使用して、レンダリングする状態テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="099d6-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="099d6-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="099d6-132">See also</span></span>



[<span data-ttu-id="099d6-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="099d6-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="099d6-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="099d6-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="099d6-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="099d6-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="099d6-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="099d6-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="099d6-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="099d6-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="099d6-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="099d6-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="099d6-139">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="099d6-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="099d6-140">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="099d6-140">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="099d6-141">状態テーブル</span><span class="sxs-lookup"><span data-stu-id="099d6-141">Status Tables</span></span>](status-tables.md)

