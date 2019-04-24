---
title: imapisessiongetstatustable
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338762"
---
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="36333-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="36333-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="36333-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36333-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36333-105">状態テーブル (セッション内のすべての MAPI リソースに関する情報を含むテーブル) へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="36333-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="36333-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="36333-106">Parameters</span></span>

 <span data-ttu-id="36333-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36333-107">_ulFlags_</span></span>
  
> <span data-ttu-id="36333-108">順番文字列の列の形式を決定するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="36333-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="36333-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="36333-109">The following flag can be set:</span></span>
    
<span data-ttu-id="36333-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="36333-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="36333-111">文字列列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="36333-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="36333-112">MAPI_UNICODE フラグが設定されていない場合、文字列列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="36333-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="36333-113">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="36333-113">_lppTable_</span></span>
  
> <span data-ttu-id="36333-114">読み上げ状態テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="36333-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36333-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="36333-115">Return value</span></span>

<span data-ttu-id="36333-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="36333-116">S_OK</span></span> 
  
> <span data-ttu-id="36333-117">テーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="36333-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36333-118">解説</span><span class="sxs-lookup"><span data-stu-id="36333-118">Remarks</span></span>

<span data-ttu-id="36333-119">**imapisession:: getstatustable**メソッドは、セッション内のすべての MAPI リソースに関する情報を含む状態テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="36333-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="36333-120">このテーブルには、mapi サブシステムに関する情報、mapi スプーラーの1行、統合アドレス帳の1行、プロファイル内のサービスプロバイダーごとに1つの行があります。</span><span class="sxs-lookup"><span data-stu-id="36333-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="36333-121">[状態] テーブルの必須およびオプションの列の完全な一覧については、「 [status Tables](status-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="36333-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="36333-122">_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、 [imapitable:: querycolumns](imapitable-querycolumns.md)および[imapitable:: QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="36333-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="36333-123">このフラグは、 [IMAPITable:: querysortorder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序で、プロパティの種類を制御することもできます。</span><span class="sxs-lookup"><span data-stu-id="36333-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="36333-124">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="36333-124">MFCMAPI reference</span></span>

<span data-ttu-id="36333-125">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="36333-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="36333-126">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="36333-126">**File**</span></span>|<span data-ttu-id="36333-127">**関数**</span><span class="sxs-lookup"><span data-stu-id="36333-127">**Function**</span></span>|<span data-ttu-id="36333-128">**コメント**</span><span class="sxs-lookup"><span data-stu-id="36333-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36333-129">maindlg .cpp</span><span class="sxs-lookup"><span data-stu-id="36333-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="36333-130">CMainDlg:: onstatustable</span><span class="sxs-lookup"><span data-stu-id="36333-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="36333-131">mfcmapi は、 **imapisession:: getstatustable**メソッドを使用して、レンダリングされる状態テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="36333-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36333-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="36333-132">See also</span></span>



[<span data-ttu-id="36333-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36333-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="36333-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="36333-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="36333-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="36333-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="36333-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="36333-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="36333-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="36333-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="36333-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="36333-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="36333-139">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="36333-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="36333-140">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="36333-140">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="36333-141">状態テーブル</span><span class="sxs-lookup"><span data-stu-id="36333-141">Status Tables</span></span>](status-tables.md)

