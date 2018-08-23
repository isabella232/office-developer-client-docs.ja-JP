---
title: サービス プロバイダーの構成の確認
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dc23dc61-7b51-43ab-a184-ce0bdac91d03
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 047a3b99b2d615984252071a1264521a4b2240f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804215"
---
# <a name="verifying-service-provider-configuration"></a>サービス プロバイダーの構成の確認
  
**適用対象**: Outlook 
  
([IABProvider::Logon](iabprovider-logon.md)、 [IMSProvider::Logon](imsprovider-logon.md)、または[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)) は、logon メソッドは、プロバイダーの構成を確認してください。 これには、すべての完全な運用に必要なプロパティが正しく設定されてチェックが含まれます。 すべてのプロバイダーのプロパティ数を変更する必要があります。構成は、プロバイダーとを許可するユーザーの介入の度合いによって異なります。 サービス プロバイダーによっては、プロファイルに必要なプロパティのすべてをしてください。 

他のサービス プロバイダーでは、プロファイルのプロパティのセットの一部を保持し、欠落している値をユーザーに確認します。 他のプロバイダーに格納しないでプロパティ、プロファイル、ユーザーはすべての構成に必要な情報に依存しています。
  
### <a name="to-retrieve-properties-stored-in-the-profile"></a>プロファイルに格納されているプロパティを取得するには
  
1. [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)、入力パラメーターとして、プロバイダーの[MAPIUID](mapiuid.md)を渡すことを呼び出します。 
    
2. 個々 のプロパティまたはプロパティの一覧を取得するためにプロファイル セクションの[IMAPIProp::GetProps](imapiprop-getprops.md)または[IMAPIProp::GetPropList](imapiprop-getproplist.md)のメソッドを呼び出します。 
    
### <a name="to-set-properties-from-user-information"></a>ユーザー情報のプロパティを設定するのには
  
MAPI では、表示を禁止するフラグを設定していない場合、プロパティ シートを表示します。 次のフラグは、ユーザー インターフェイスを表示できないことを示します。
  
|**Flag**|**サービス プロバイダー**|
|:-----|:-----|
|AB_NO_DIALOG  <br/> |アドレス帳プロバイダー  <br/> |
|LOGON_NO_DIALOG  <br/> |トランスポート プロバイダー  <br/> |
|MDB_NO_DIALOG  <br/> |メッセージ ストア プロバイダー  <br/> |
   
場合は、プロバイダーに保存しません。 すべての構成プロパティ、プロファイル、ユーザーの介入を必要とするし、MAPI ダイアログ ボックスの抑制のフラグのいずれかのログオン方法として、MAPI_E_UNCONFIGURED を返します。 ダイアログの抑制のフラグが設定されていないが、ユーザーがすべての必要な情報を提供しない場合もこのエラーを返します。
  
サービス ・ プロバイダーには、MAPI_E_UNCONFIGURED では、そのログオン方法が失敗した場合、MAPI は、エントリ ポイント関数をもう一度呼び出します。 情報を 2 番目の呼び出しを特定できない場合は、サービス プロバイダーの重要度に応じて、そのセッション可能性があります終了します。 
  
次の図は、サービス プロバイダーのログオン方法の構成に必要なロジックを示します。 
  
**構成検証のフローチャート**
  
![構成の確認フローチャート](media/amapi_62.gif "構成の確認フローチャート")
  
## <a name="see-also"></a>関連項目

- [サービス プロバイダー ログオンの実装](implementing-service-provider-logon.md)

