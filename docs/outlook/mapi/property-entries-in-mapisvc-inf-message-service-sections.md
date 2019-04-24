---
title: mapisvc.inf メッセージサービスセクションのプロパティエントリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328519"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="ffc71-103">mapisvc.inf メッセージサービスセクションのプロパティエントリ</span><span class="sxs-lookup"><span data-stu-id="ffc71-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="ffc71-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffc71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffc71-105">プロパティを設定するエントリは、次の形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="ffc71-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="ffc71-106">**プロパティタグ\*\*\*\*=** プロパティ値</span><span class="sxs-lookup"><span data-stu-id="ffc71-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="ffc71-107">構成データが mapi で定義されたプロパティの1つを表している場合、またはデータが mapi プロパティを表していない場合は標準でないタグとして、プロパティタグを標準の mapi プロパティタグにすることができます。</span><span class="sxs-lookup"><span data-stu-id="ffc71-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="ffc71-108">非標準のタグは、プロパティの識別子の値とプロパティの型を結合することによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="ffc71-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="ffc71-109">結果は8桁の16進数値になります。</span><span class="sxs-lookup"><span data-stu-id="ffc71-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="ffc71-110">プロパティの値には、どのような意味でプロパティタグを指定できます。</span><span class="sxs-lookup"><span data-stu-id="ffc71-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="ffc71-111">メッセージサービスセクションには、構成されているメッセージサービスに応じて、さまざまなエントリを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ffc71-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="ffc71-112">通常、次の MAPI プロパティは、表示されている形式のメッセージサービスセクションに含まれています。</span><span class="sxs-lookup"><span data-stu-id="ffc71-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="ffc71-113">**PR_DISPLAY_NAME** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="ffc71-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="ffc71-114">\*\*\*\* =  _DLL ファイルの PR_SERVICE_DLL_NAME 名_</span><span class="sxs-lookup"><span data-stu-id="ffc71-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="ffc71-115">\*\*\*\* =  _エントリポイント関数の PR_SERVICE_ENTRY_NAME 名_</span><span class="sxs-lookup"><span data-stu-id="ffc71-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="ffc71-116">**PR_SERVICE_SUPPORT_FILES** =  _ファイルの一覧_</span><span class="sxs-lookup"><span data-stu-id="ffc71-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="ffc71-117">**PR_SERVICE_DELETE_FILES** =  _ファイルの一覧_</span><span class="sxs-lookup"><span data-stu-id="ffc71-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="ffc71-118">**PR_RESOURCE_FLAGS** =  _ビットマスク_</span><span class="sxs-lookup"><span data-stu-id="ffc71-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="ffc71-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 文字列は、ユーザーインターフェイスに表示されるメッセージサービスの名前です。これは、ユーザーがメッセージサービスと関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="ffc71-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="ffc71-120">表示名は、mapisvc.inf の省略可能なエントリです。</span><span class="sxs-lookup"><span data-stu-id="ffc71-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="ffc71-121">表示名は2つの部分で構成される場合があります。メッセージサービスによって割り当てられたパーツと、ユーザーによって割り当てられたパーツ。</span><span class="sxs-lookup"><span data-stu-id="ffc71-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="ffc71-122">ユーザーがいずれかのパーツの割り当てを担当している場合は、通常、クライアントアプリケーションのコントロールの下に、メッセージサービスによって提供されるプロパティシートとして知られる特別なダイアログボックスで処理されます。</span><span class="sxs-lookup"><span data-stu-id="ffc71-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="ffc71-123">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) エントリに提供される情報は、メッセージサービスを含む DLL の名前です。</span><span class="sxs-lookup"><span data-stu-id="ffc71-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="ffc71-124">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) エントリに提供されている情報は、MAPI がメッセージサービスを構成するために呼び出す DLL 内のエントリポイント関数の名前です。</span><span class="sxs-lookup"><span data-stu-id="ffc71-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="ffc71-125">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) エントリに記載されているファイルは、メッセージサービスと共にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffc71-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="ffc71-126">同様に、メッセージサービスが削除されたときに、 **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) エントリ内のファイルを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffc71-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="ffc71-127">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) エントリは、メッセージサービスに対して定義されたオプションのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="ffc71-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="ffc71-128">たとえば、SERVICE_SINGLE_COPY ビットは、メッセージサービスが特定のプロファイルに一度しか表示されない場合に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ffc71-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="ffc71-129">メッセージサービスが id 情報を提供しない場合は、SERVICE_NO_PRIMARY_IDENTITY ビットが設定されます。</span><span class="sxs-lookup"><span data-stu-id="ffc71-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="ffc71-130">標準的でないプロパティエントリの2つの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ffc71-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="ffc71-131">最初のエントリは、プロパティ値として既定のアドレス帳で使用されるファイルへのパスを指定します。2番目のエントリは、数値プロパティ値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ffc71-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="ffc71-132">両方のエントリが AB メッセージサービスに固有のものであることを意味します。</span><span class="sxs-lookup"><span data-stu-id="ffc71-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


