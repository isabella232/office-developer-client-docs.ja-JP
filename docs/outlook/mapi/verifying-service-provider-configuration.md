---
title: サービス プロバイダー構成の検証
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 381e2c9ec84811b69d666017a568e7b9cca21755
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329609"
---
# <a name="verifying-service-provider-configuration"></a>サービス プロバイダー構成の検証
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ログオン方法 ([IABProvider:: logon](iabprovider-logon.md)、 [IMSProvider:: logon](imsprovider-logon.md)、または[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)) は、プロバイダーの構成を確認する必要があります。 これには、完全な操作に必要なすべてのプロパティが正しく設定されていることを確認する必要があります。 すべてのプロバイダーは、異なる数のプロパティを必要とします。構成は、プロバイダーと、許可するユーザー操作の程度によって異なります。 一部のサービスプロバイダーは、必要なすべてのプロパティをプロファイルに保持します。 

その他のサービスプロバイダーは、プロファイルにプロパティの一部のセットを保持し、ユーザーに不足している値を要求します。 それでも、他のプロバイダーはプロファイルにプロパティを保存しません。また、構成に必要なすべての情報をユーザーが指定できるようにします。
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a>プロファイルに格納されているプロパティを取得するには
  
1. [MAPIUID](mapiuid.md)を入力パラメーターとして渡して、 [imapisupport:: openプロファイル](imapisupport-openprofilesection.md)を呼び出します。 
    
2. プロファイルセクションの[imapiprop:: GetProps](imapiprop-getprops.md)または[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドを呼び出して、個々のプロパティまたはプロパティリストを取得します。 
    
### <a name="to-set-properties-from-user-information"></a>ユーザー情報からプロパティを設定するには
  
MAPI が表示の禁止フラグを設定していない場合は、プロパティシートを表示します。 次のフラグは、ユーザーインターフェイスを表示できないことを示します。
  
|**Flag**|**サービスプロバイダー**|
|:-----|:-----|
|AB_NO_DIALOG  <br/> |アドレス帳プロバイダー  <br/> |
|LOGON_NO_DIALOG  <br/> |トランスポートプロバイダー  <br/> |
|MDB_NO_DIALOG  <br/> |メッセージストアプロバイダー  <br/> |
   
プロバイダーがプロファイルにすべての構成プロパティを格納せず、ユーザーの操作を必要とし、MAPI がログオン方法にダイアログボックス抑制フラグの1つを渡す場合は、MAPI_E_UNCONFIGURED を返します。 ダイアログ抑制フラグが設定されていないが、ユーザーが必要な情報をすべて指定していない場合にも、このエラーを返します。
  
サービスプロバイダーが MAPI_E_UNCONFIGURED を使用してログオン方法に失敗すると、MAPI はエントリポイント関数を再度呼び出します。 2番目の呼び出しで情報が見つからない場合は、サービスプロバイダーの重要度によってはセッションが終了する可能性があります。 
  
次の図は、サービスプロバイダーのログオン方法での構成に必要なロジックを示しています。 
  
**構成検証のフローチャート**
  
![構成検証のフローチャート](media/amapi_62.gif "構成検証のフローチャート")
  
## <a name="see-also"></a>関連項目

- [サービスプロバイダーログオンの実装](implementing-service-provider-logon.md)

