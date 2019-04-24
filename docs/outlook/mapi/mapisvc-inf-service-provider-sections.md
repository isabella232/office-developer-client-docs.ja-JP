---
title: mapisvc.inf サービスプロバイダーのセクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ea192ec6356cc3b929bf8379567144d3a54223f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309542"
---
# <a name="mapisvcinf-service-provider-sections"></a>mapisvc.inf サービスプロバイダーのセクション

**適用対象**: Outlook 2013 | Outlook 2016 
  
mapisvc.inf には、前の「メッセージサービス」セクションの**プロバイダ**エントリにリストされている各エントリのサービスプロバイダセクションが含まれています。 **サービス**プロバイダーのセクションは、両方の種類のセクションに次の形式のエントリが含まれているという点で、メッセージサービスセクションに似ています。 
  
**プロパティタグ**= プロパティ値 
  
ただし、サービスプロバイダーのセクションとメッセージサービスのセクションは、このようなプロパティエントリがサービスプロバイダーセクションに含まれるエントリの唯一の種類であるという点で異なります。 サービスプロバイダーには、追加またはリンクされたセクションはありません。すべてのサービスプロバイダー情報は、1つのセクション内に含める必要があります。 
  
[メッセージサービス] セクションで設定されているプロパティの一部は、[サービスプロバイダ] セクションでも設定されています。これらのプロパティは両方にとって有効です。 **PR_DISPLAY_NAME**プロパティの例を次に示します。 サービスプロバイダーとメッセージサービスの両方には、構成ユーザーインターフェイスでの表示に使用される名前があります。 この名前は、サービスプロバイダーによって異なりますが、同じでもかまいません。 その他のプロパティは、サービスプロバイダーに固有のものです。 
  
サービスプロバイダーの一般的なセクションには、次のエントリが含まれています。これらはすべて必要です。
  
**PR_DISPLAY_NAME** =  _文字列_
  
**PR_PROVIDER_DISPLAY** =  _文字列_
  
**** =  _DLL ファイルの PR_PROVIDER_DLL_NAME 名_
  
**PR_RESOURCE_TYPE** =  _long_
  
**PR_RESOURCE_FLAGS** =  _ビットマスク_
  
**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) エントリは**PR_SERVICE_DLL_NAME**に似ています。これは、サービスプロバイダーを含む DLL のファイル名を示します。 メッセージサービスコードは、サービスプロバイダーの1つと同じ dll ファイルに格納するか、別の dll として存在することができます。 ターゲットプラットフォームに関係なく、エントリにサフィックスが含まれていないことに注意してください。MAPI は必要に応じてサフィックスを追加します。 
  
**PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry は、サービスプロバイダーの種類を表します。サービスプロバイダーは、それを適切な定義済みの定数に設定します。 有効な値は、MAPI_STORE_PROVIDER、MAPI_TRANSPORT_PROVIDER、および MAPI_AB_PROVIDER です。
  
メッセージサービスとサービスプロバイダーの両方に適用される別のプロパティエントリは、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) エントリがオプションを示します。 このプロパティエントリの設定は、サービスプロバイダーによって異なる場合があります。 たとえば、一部のメッセージストアプロバイダーでは、 **PR_RESOURCE_FLAGS**が既定のメッセージストアとして機能しない場合、STATUS_NO_DEFAULT_STORE に設定されている場合があります。 
  
次に、サービスプロバイダーセクションの3つの例を示します。 **[AB provider]** セクションは、既定のアドレス帳サービスのサービスプロバイダーセクションです。 **[msgservice Prov1]** および **[msgservice Prov2]** セクションは、自分のサービスに属しています。1つ目はアドレス帳プロバイダーセクションで、2つ目はメッセージストアプロバイダーセクションです。 
  
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


