---
title: MapiSvc.inf メッセージ サービス セクション内のプロパティ エントリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 30f5e0b59bacfab91a3a6c77c0b345d6299df9e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803688"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="46f7f-103">MapiSvc.inf メッセージ サービス セクション内のプロパティ エントリ</span><span class="sxs-lookup"><span data-stu-id="46f7f-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="46f7f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46f7f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46f7f-105">プロパティを設定するエントリは、この形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="46f7f-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="46f7f-106">**プロパティ タグ****=** プロパティの値</span><span class="sxs-lookup"><span data-stu-id="46f7f-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="46f7f-107">プロパティ タグは、データが MAPI プロパティを表していない場合の標準的な MAPI プロパティ タグの構成データを表している場合で MAPI では、定義済みのプロパティのいずれかまたは非標準のタグにあります。</span><span class="sxs-lookup"><span data-stu-id="46f7f-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="46f7f-108">非標準のタグがプロパティの型とプロパティの識別子の値を組み合わせることによって行われます。</span><span class="sxs-lookup"><span data-stu-id="46f7f-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="46f7f-109">8 桁の 16 進数になります。</span><span class="sxs-lookup"><span data-stu-id="46f7f-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="46f7f-110">プロパティ タグの意味は、どのようなプロパティを指定できます。</span><span class="sxs-lookup"><span data-stu-id="46f7f-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="46f7f-111">メッセージ サービスのセクションでは、さまざまなエントリによって構成されているメッセージ サービスを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="46f7f-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="46f7f-112">一覧の形式でメッセージのサービス] セクションでは、次の MAPI プロパティが含まれます通常。</span><span class="sxs-lookup"><span data-stu-id="46f7f-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="46f7f-113">**PR_DISPLAY_NAME** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="46f7f-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="46f7f-114">**PR_SERVICE_DLL_NAME** =  _DLL ファイルの名前_</span><span class="sxs-lookup"><span data-stu-id="46f7f-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="46f7f-115">**PR_SERVICE_ENTRY_NAME** =  _エントリ ポイント関数の名前_</span><span class="sxs-lookup"><span data-stu-id="46f7f-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="46f7f-116">**PR_SERVICE_SUPPORT_FILES** =  _ファイルの一覧_</span><span class="sxs-lookup"><span data-stu-id="46f7f-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="46f7f-117">**PR_SERVICE_DELETE_FILES** =  _ファイルの一覧_</span><span class="sxs-lookup"><span data-stu-id="46f7f-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="46f7f-118">**PR_RESOURCE_FLAGS** =  _ビットマスク_</span><span class="sxs-lookup"><span data-stu-id="46f7f-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="46f7f-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) の文字列は、ユーザーはメッセージ サービスに関連付けられた名前であり、ユーザー インターフェイスに表示されるメッセージ サービスの名前です。</span><span class="sxs-lookup"><span data-stu-id="46f7f-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="46f7f-120">表示名は、mapisvc.inf の省略可能なエントリです。</span><span class="sxs-lookup"><span data-stu-id="46f7f-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="46f7f-121">ふたつの部分表示名を作成する場合があります。メッセージ サービスによって割り当てられた部品と、ユーザーが割り当てられている部品です。</span><span class="sxs-lookup"><span data-stu-id="46f7f-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="46f7f-122">ユーザーが部品の 1 つの割り当てを担当する場合は、通常クライアント アプリケーションの制御下にあるメッセージ サービスによって提供されるプロパティ シートと呼ばれる特別なダイアログ ボックスで処理します。</span><span class="sxs-lookup"><span data-stu-id="46f7f-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="46f7f-123">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) のエントリの情報は、メッセージ サービスを含む DLL の名前です。</span><span class="sxs-lookup"><span data-stu-id="46f7f-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="46f7f-124">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) のエントリの情報は、メッセージ サービスを構成するのには MAPI の呼び出しをその DLL 内のエントリ ポイント関数の名前です。</span><span class="sxs-lookup"><span data-stu-id="46f7f-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="46f7f-125">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) のエントリに記載されているファイルは、メッセージ サービスをインストールする必要があるファイルです。</span><span class="sxs-lookup"><span data-stu-id="46f7f-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="46f7f-126">同様に、メッセージ サービスが削除されたときは、 **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) のエントリ内のファイルを削除してください。</span><span class="sxs-lookup"><span data-stu-id="46f7f-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="46f7f-127">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) のエントリは、メッセージ サービスに対して定義されているオプションの集合です。</span><span class="sxs-lookup"><span data-stu-id="46f7f-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="46f7f-128">たとえば、メッセージ サービスが一度だけ表示されます、特定のプロファイルの場合、SERVICE_SINGLE_COPY ビットが設定されます。</span><span class="sxs-lookup"><span data-stu-id="46f7f-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="46f7f-129">メッセージ サービスが id 情報を提供していない場合、SERVICE_NO_PRIMARY_IDENTITY ビットが設定されています。</span><span class="sxs-lookup"><span data-stu-id="46f7f-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="46f7f-130">非標準のプロパティ エントリの 2 つの例に従います。</span><span class="sxs-lookup"><span data-stu-id="46f7f-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="46f7f-131">最初のエントリは、プロパティの値として既定のアドレス帳で使用されるファイルへのパスを指定します。2 番目のエントリでは、数値プロパティの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="46f7f-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="46f7f-132">両方のエントリには、AB のメッセージ サービスに固有の意味があります。</span><span class="sxs-lookup"><span data-stu-id="46f7f-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


