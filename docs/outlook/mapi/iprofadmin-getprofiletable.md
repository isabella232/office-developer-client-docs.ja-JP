---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309549"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="82d48-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="82d48-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="82d48-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82d48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82d48-105">利用可能なすべてのプロファイルについての情報を含むテーブルである、プロファイルテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="82d48-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="82d48-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="82d48-106">Parameters</span></span>

 <span data-ttu-id="82d48-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="82d48-107">_ulFlags_</span></span>
  
> <span data-ttu-id="82d48-108">順番常に NULL。</span><span class="sxs-lookup"><span data-stu-id="82d48-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="82d48-109">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="82d48-109">_lppTable_</span></span>
  
> <span data-ttu-id="82d48-110">読み上げプロファイルテーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="82d48-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="82d48-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="82d48-111">Return value</span></span>

<span data-ttu-id="82d48-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="82d48-112">S_OK</span></span> 
  
> <span data-ttu-id="82d48-113">プロファイルテーブルが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="82d48-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82d48-114">解説</span><span class="sxs-lookup"><span data-stu-id="82d48-114">Remarks</span></span>

<span data-ttu-id="82d48-115">**IProfAdmin:: getprofiletable**メソッドはプロファイルテーブルへのアクセスを提供します。これには、使用可能なすべてのプロファイルに対応する1つの行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="82d48-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="82d48-116">各行には、プロファイルの表示名、およびプロファイルが既定であるかどうかを示すフラグの2つの列のみがあります。</span><span class="sxs-lookup"><span data-stu-id="82d48-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="82d48-117">削除されているか、使用されているが削除対象としてマークされているプロファイルは、プロファイルテーブルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="82d48-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="82d48-118">プロファイルテーブルは静的です。後でプロファイルを追加または削除しても、テーブルには反映されません。</span><span class="sxs-lookup"><span data-stu-id="82d48-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="82d48-119">プロファイルが存在しない場合、 **getprofiletable**は、行数が0のテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="82d48-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="82d48-120">プロファイルテーブルの詳細については、「 [profile Tables](profile-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82d48-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="82d48-121">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="82d48-121">MFCMAPI reference</span></span>

<span data-ttu-id="82d48-122">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82d48-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="82d48-123">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="82d48-123">**File**</span></span>|<span data-ttu-id="82d48-124">**関数**</span><span class="sxs-lookup"><span data-stu-id="82d48-124">**Function**</span></span>|<span data-ttu-id="82d48-125">**コメント**</span><span class="sxs-lookup"><span data-stu-id="82d48-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="82d48-126">maindlg .cpp</span><span class="sxs-lookup"><span data-stu-id="82d48-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="82d48-127">CMainDlg:: onshowprofiles</span><span class="sxs-lookup"><span data-stu-id="82d48-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="82d48-128">mfcmapi は、 **IProfAdmin:: getprofiletable**メソッドを使用して、新しいダイアログボックスに表示するプロファイルテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="82d48-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82d48-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="82d48-129">See also</span></span>



[<span data-ttu-id="82d48-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="82d48-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="82d48-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="82d48-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="82d48-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="82d48-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


<span data-ttu-id="82d48-133">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="82d48-133">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

