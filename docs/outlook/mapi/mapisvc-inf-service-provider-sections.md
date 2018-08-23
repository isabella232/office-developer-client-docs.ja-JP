---
title: MapiSvc.inf サービス プロバイダーセクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 05666d8d6b7279588b4b442151640fa1696aedda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586782"
---
# <a name="mapisvcinf-service-provider-sections"></a>MapiSvc.inf サービス プロバイダーセクション

**適用されます**: Outlook 2013 |Outlook 2016 
  
Mapisvc.inf には、メッセージ サービスの前のセクションで**プロバイダー**のエントリに記載されているエントリのそれぞれのサービス プロバイダーの 1 つのセクションが含まれています。 **サービス**プロバイダー セクションと似ていますがメッセージ サービスのセクションでセクションの両方の種類には、この形式のエントリが含まれています。 
  
**プロパティ タグ**プロパティの値を = 
  
ただし、サービスのプロバイダー セクションで、メッセージ サービスのセクションとは異なりそのようなプロパティのエントリは、サービスのプロバイダー セクションに含まれているエントリの種類。 必要があります追加またはリンクのセクションで、サービス プロバイダーです。1 つのセクション内では、すべてのサービス プロバイダーの情報を含める必要があります。 
  
メッセージ サービスのセクションで設定されているプロパティのいくつかは、これらのプロパティは、両方の意味を行うために、サービス プロバイダーのセクションで設定もできます。 **PR_DISPLAY_NAME**プロパティは、例です。 構成のユーザー インターフェイスに表示するために使用される名前は、サービス プロバイダーとサービスのメッセージの両方であります。 サービス プロバイダーによってその名可能性がありますか、同じことができません。 その他のプロパティは、サービス ・ プロバイダーに固有です。 
  
プロバイダー セクションの一般的なサービスには、必要なすべてが、次のエントリがあります。
  
**PR_DISPLAY_NAME** =  _の文字列_
  
**PR_PROVIDER_DISPLAY** =  _の文字列_
  
**PR_PROVIDER_DLL_NAME** =  _DLL ファイルの名前_
  
**PR_RESOURCE_TYPE** =  _長_
  
**PR_RESOURCE_FLAGS** =  _ビットマスク_
  
**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) のエントリが**PR_SERVICE_DLL_NAME**に似ています。サービス プロバイダーを含む DLL のファイル名を示します。 メッセージ サービスのコードは、同じ DLL ファイル内のサービス ・ プロバイダーのいずれかで保存することがありますか、別の DLL として存在しています。 ターゲット プラットフォームに関係なく、エントリにサフィックスが含まれていないことに注意してください。MAPI の必要な場合にサフィックスを追加することによって行われます。 
  
**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md)) のエントリは、サービス プロバイダーの種類を表します。サービス プロバイダーは、適切な定義済みの定数を設定します。 有効な値には、MAPI_STORE_PROVIDER、MAPI_TRANSPORT_PROVIDER、および MAPI_AB_PROVIDER が含まれます。
  
メッセージ サービスおよびサービス ・ プロバイダーの両方に適用される他のプロパティ エントリ、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) のエントリは、オプションを指定します。 このプロパティのエントリの設定は、サービス プロバイダーによって異なります。 たとえば、メッセージ ストアのプロバイダーによって設定**PR_RESOURCE_FLAGS** STATUS_NO_DEFAULT_STORE に既定のメッセージ ストアとして動作しない場合。 
  
サービス プロバイダー セクションの 3 つの例に従います。 **[AB プロバイダー]** セクションでは、既定のアドレス帳サービスのサービス プロバイダーのセクションです。 **[MsgService Prov1]** と **[MsgService Prov2]** セクションでは、自分独自のサービスです。最初のアドレス帳のプロバイダー セクションでは、2 番目のメッセージ ストア プロバイダー セクションです。 
  
```cpp
[AB Provider]
PR_DISPLAY_NAME=Default Address Book
PR_PROVIDER_DISPLAY=Default Address Book
PR_PROVIDER_DLL_NAME=AB.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
6600001e=C:\WINNT35\System32\DEFAB.TXT
[MsgService Prov1]
PR_DISPLAY_NAME=My Own Service
PR_PROVIDER_DISPLAY=My Own Address Book
PR_PROVIDER_DLL_NAME=MYXXX.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
[MsgService Prov2]
PR_DISPLAY_NAME=My Folders
PR_PROVIDER_DISPLAY=My Own Message Store
PR_RESOURCE_TYPE=MAPI_STORE_PROVIDER
PR_PROVIDER_DLL_NAME=MYZZZ.DLL
PR_RESOURCE_FLAGS=STATUS_NO_DEFAULT_STORE
66060003=00000000
66030003=00000000
34140102=78b2fa70aff711cd9bc800aa002fc45a
66090003=06000000
660A0003=03000000

```


