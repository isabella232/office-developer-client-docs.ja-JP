---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e7abcb2c86ff5cabe0b8f5664ec316244617ac09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421236"
---
# <a name="direntryid"></a><span data-ttu-id="fead9-103">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fead9-103">DIR_ENTRYID</span></span>

  
  
<span data-ttu-id="fead9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fead9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fead9-105">ディレクトリエントリ id のプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fead9-105">Describes the properties of a directory entry id.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fead9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fead9-106">Header file:</span></span>  <br/> |<span data-ttu-id="fead9-107">entryid</span><span class="sxs-lookup"><span data-stu-id="fead9-107">entryid.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="fead9-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="fead9-108">Members</span></span>

 <span data-ttu-id="fead9-109">**abflags**</span><span class="sxs-lookup"><span data-stu-id="fead9-109">**abFlags**</span></span>
  
> <span data-ttu-id="fead9-110">オブジェクトについての情報を提供するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="fead9-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="fead9-111">詳細については、 [ENTRYID](entryid.md)構造の**abflags**フィールドの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fead9-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="fead9-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="fead9-112">**muid**</span></span>
  
> <span data-ttu-id="fead9-113">ストアプロバイダーを識別する GUID。</span><span class="sxs-lookup"><span data-stu-id="fead9-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="fead9-114">**ulversion**</span><span class="sxs-lookup"><span data-stu-id="fead9-114">**ulVersion**</span></span>
  
> <span data-ttu-id="fead9-115">**DIR_ENTRYID**構造体のバージョン番号。</span><span class="sxs-lookup"><span data-stu-id="fead9-115">The version number of the **DIR_ENTRYID** structure.</span></span> <span data-ttu-id="fead9-116">CONTAB_VERSION に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fead9-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="fead9-117">**ultype**</span><span class="sxs-lookup"><span data-stu-id="fead9-117">**ulType**</span></span>
  
> <span data-ttu-id="fead9-118">ディレクトリエントリ ID の種類を表す整数。</span><span class="sxs-lookup"><span data-stu-id="fead9-118">An integer representing the directory entry ID type.</span></span> <span data-ttu-id="fead9-119">次のいずれかの値であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="fead9-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="fead9-120">**名前**</span><span class="sxs-lookup"><span data-stu-id="fead9-120">**Name**</span></span>|<span data-ttu-id="fead9-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="fead9-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fead9-122">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="fead9-122">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="fead9-123">MAPI アドレス帳のルートフォルダー。</span><span class="sxs-lookup"><span data-stu-id="fead9-123">The root folder for a MAPI address book.</span></span>  <br/> |
|<span data-ttu-id="fead9-124">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="fead9-124">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="fead9-125">MAPI アドレス帳のオブジェクトのルート フォルダー内に含まれるサブフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="fead9-125">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="fead9-126">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="fead9-126">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="fead9-127">�A�h���X���̃R���e�i�[ �I�u�W�F�N�g�ł��B</span><span class="sxs-lookup"><span data-stu-id="fead9-127">An address book container object.</span></span>  <br/> |
   
 <span data-ttu-id="fead9-128">**muidID**</span><span class="sxs-lookup"><span data-stu-id="fead9-128">**muidID**</span></span>
  
> <span data-ttu-id="fead9-129">ログオンオブジェクトを識別する GUID。</span><span class="sxs-lookup"><span data-stu-id="fead9-129">A GUID that identifies the logon object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fead9-130">注釈</span><span class="sxs-lookup"><span data-stu-id="fead9-130">Remarks</span></span>

<span data-ttu-id="fead9-131">**DIR_ENTRYID**と[CONTAB_ENTRYID](contab_entryid.md)の構造は同じですが、 **ultype**メンバーを除きます。</span><span class="sxs-lookup"><span data-stu-id="fead9-131">The structures **DIR_ENTRYID** and [CONTAB_ENTRYID](contab_entryid.md) are identical, except for the **ulType** member.</span></span> <span data-ttu-id="fead9-132">**ultype**メンバーの内容は、残りのフィールドに適した構造を決定します。</span><span class="sxs-lookup"><span data-stu-id="fead9-132">The contents of the **ulType** member determine which structure is appropriate for the remaining fields.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fead9-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="fead9-133">See also</span></span>



[<span data-ttu-id="fead9-134">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fead9-134">CONTAB_ENTRYID</span></span>](contab_entryid.md)


[<span data-ttu-id="fead9-135">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="fead9-135">MAPI Structures</span></span>](mapi-structures.md)

