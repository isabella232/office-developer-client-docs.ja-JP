---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9ef3f37ab266469e83434d5d9bd0bc7e2ef897fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583345"
---
# <a name="direntryid"></a><span data-ttu-id="a43b3-103">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a43b3-103">DIR_ENTRYID</span></span>

  
  
<span data-ttu-id="a43b3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a43b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a43b3-105">ディレクトリのエントリ id のプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a43b3-105">Describes the properties of a directory entry id.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a43b3-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a43b3-106">Header file:</span></span>  <br/> |<span data-ttu-id="a43b3-107">entryid.h</span><span class="sxs-lookup"><span data-stu-id="a43b3-107">entryid.h</span></span>  <br/> |
   
```cpp
#pragma pack(4)
typedef struct _dir_entryid
{
    BYTE abFlags[4]; 
    MAPIUID muid; 
    ULONG ulVersion; 
    ULONG ulType; 
    MAPIUID muidID; 
}   DIR_ENTRYID, *LPDIR_ENTRYID; 
#pragma pack()
```

## <a name="members"></a><span data-ttu-id="a43b3-108">Members</span><span class="sxs-lookup"><span data-stu-id="a43b3-108">Members</span></span>

 <span data-ttu-id="a43b3-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="a43b3-109">**abFlags**</span></span>
  
> <span data-ttu-id="a43b3-110">オブジェクトを記述する情報を提供するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="a43b3-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="a43b3-111">詳細については、[エントリ ID](entryid.md)の構造体の**abFlags**フィールドの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a43b3-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="a43b3-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="a43b3-112">**muid**</span></span>
  
> <span data-ttu-id="a43b3-113">ストア プロバイダーを識別する GUID。</span><span class="sxs-lookup"><span data-stu-id="a43b3-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="a43b3-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="a43b3-114">**ulVersion**</span></span>
  
> <span data-ttu-id="a43b3-115">**DIR_ENTRYID**構造体のバージョン番号です。</span><span class="sxs-lookup"><span data-stu-id="a43b3-115">The version number of the **DIR_ENTRYID** structure.</span></span> <span data-ttu-id="a43b3-116">CONTAB_VERSION に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a43b3-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="a43b3-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="a43b3-117">**ulType**</span></span>
  
> <span data-ttu-id="a43b3-118">ディレクトリ エントリ ID の種類を表す整数。</span><span class="sxs-lookup"><span data-stu-id="a43b3-118">An integer representing the directory entry ID type.</span></span> <span data-ttu-id="a43b3-119">次の値のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a43b3-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="a43b3-120">**名前**</span><span class="sxs-lookup"><span data-stu-id="a43b3-120">**Name**</span></span>|<span data-ttu-id="a43b3-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="a43b3-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a43b3-122">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="a43b3-122">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="a43b3-123">MAPI アドレス帳のルート フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="a43b3-123">The root folder for a MAPI address book.</span></span>  <br/> |
|<span data-ttu-id="a43b3-124">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="a43b3-124">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="a43b3-125">MAPI アドレス帳のオブジェクトのルート フォルダー内に含まれるサブフォルダー。</span><span class="sxs-lookup"><span data-stu-id="a43b3-125">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="a43b3-126">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="a43b3-126">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="a43b3-127">�A�h���X���̃R���e�i�[ �I�u�W�F�N�g�ł��B</span><span class="sxs-lookup"><span data-stu-id="a43b3-127">An address book container object.</span></span>  <br/> |
   
 <span data-ttu-id="a43b3-128">**muidID**</span><span class="sxs-lookup"><span data-stu-id="a43b3-128">**muidID**</span></span>
  
> <span data-ttu-id="a43b3-129">ログオン オブジェクトを識別する GUID です。</span><span class="sxs-lookup"><span data-stu-id="a43b3-129">A GUID that identifies the logon object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a43b3-130">注釈</span><span class="sxs-lookup"><span data-stu-id="a43b3-130">Remarks</span></span>

<span data-ttu-id="a43b3-131">**DIR_ENTRYID**と[CONTAB_ENTRYID](contab_entryid.md)の構造体では、 **ulType**メンバーを除くと同じです。</span><span class="sxs-lookup"><span data-stu-id="a43b3-131">The structures **DIR_ENTRYID** and [CONTAB_ENTRYID](contab_entryid.md) are identical, except for the **ulType** member.</span></span> <span data-ttu-id="a43b3-132">**UlType**メンバーの内容は、どの構造体は、残りのフィールドの適切なを確認します。</span><span class="sxs-lookup"><span data-stu-id="a43b3-132">The contents of the **ulType** member determine which structure is appropriate for the remaining fields.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a43b3-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="a43b3-133">See also</span></span>



[<span data-ttu-id="a43b3-134">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="a43b3-134">CONTAB_ENTRYID</span></span>](contab_entryid.md)


[<span data-ttu-id="a43b3-135">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="a43b3-135">MAPI Structures</span></span>](mapi-structures.md)

