---
title: MapiSvc.inf サービス プロバイダーのセクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 276d9e8d96d620060ea1cf3bac5790f34a900efd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551143"
---
# <a name="mapisvcinf-service-provider-sections"></a>MapiSvc.inf サービス プロバイダーのセクション

**適用対象**: Outlook 2013 | Outlook 2016 
  
Mapisvc.inf には、前のメッセージ サービス セクションの **Providers** エントリに記載されている各エントリに対して 1 つのサービス プロバイダー セクションが含まれています。 **サービス** プロバイダー のセクションは、両方の種類のセクションにこの形式のエントリが含まれるという点で、メッセージ サービス セクションに似ています。 
  
**プロパティ タグ** = プロパティ値 
  
ただし、サービス プロバイダー セクションとメッセージ サービス セクションは、このようなプロパティ エントリがサービス プロバイダー セクションに含まれる唯一の種類のエントリである点で異なります。 サービス プロバイダーの追加またはリンクされたセクションはありません。すべてのサービス プロバイダー情報は、1 つのセクションに含まれている必要があります。 
  
これらのプロパティは両方とも意味を持つため、メッセージ サービス セクションで設定されているプロパティの一部は、サービス プロバイダー セクションでも設定されます。 プロパティ **PR_DISPLAY_NAME** 例を示します。 サービス プロバイダーとメッセージ サービスの両方に、構成ユーザー インターフェイスでの表示に使用される名前があります。 サービス プロバイダーによっては、その名前が同じか異なる場合があります。 その他のプロパティは、サービス プロバイダーに固有です。 
  
一般的なサービス プロバイダー のセクションには、次のエントリが含まれます。そのすべてが必須です。
  
**PR_DISPLAY_NAME**  =  _string_
  
**PR_PROVIDER_DISPLAY**  =  _string_
  
**PR_PROVIDER_DLL_NAME**  =  _DLL ファイルの名前_
  
**PR_RESOURCE_TYPE**  =  _long_
  
**PR_RESOURCE_FLAGS**  =  _ビットマスク_
  
この **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) エントリは、次の **PR_SERVICE_DLL_NAME。** サービス プロバイダーを含む DLL のファイル名を示します。 メッセージ サービス コードは、サービス プロバイダーの 1 つを同じ DLL ファイルに格納するか、別の DLL として存在することができます。 ターゲット プラットフォームに関係なく、エントリに接尾辞が含まれていない点に注意してください。MAPI は、必要に応じて接尾辞の追加を行います。 
  
**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) エントリは、サービス プロバイダーの種類を表します。サービス プロバイダーは、それを適切な定義済みの定数に設定します。 有効な値には、MAPI_STORE_PROVIDER、MAPI_TRANSPORT_PROVIDER、およびMAPI_AB_PROVIDER。
  
メッセージ サービスとサービス プロバイダーの両方に適用される別のプロパティ エントリで、PR_RESOURCE_FLAGS **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) エントリはオプションを示します。 このプロパティ エントリの設定は、サービス プロバイダーによって異なる場合があります。 たとえば、一部のメッセージ ストア プロバイダーは、既定のメッセージ PR_RESOURCE_FLAGSとしてSTATUS_NO_DEFAULT_STORE機能しない場合に、メッセージ ストアプロバイダーを既定のメッセージ ストアに設定する場合があります。 
  
サービス プロバイダーセクションの 3 つの例を次に示します。 [AB **プロバイダー] セクションは** 、既定のアドレス帳サービスのサービス プロバイダー セクションです。 **[MsgService Prov1] セクションと** **[MsgService Prov2]** セクションは、My Own Service に属します。1 つ目はアドレス帳プロバイダー セクションで、2 つ目はメッセージ ストア プロバイダー セクションです。 
  
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


