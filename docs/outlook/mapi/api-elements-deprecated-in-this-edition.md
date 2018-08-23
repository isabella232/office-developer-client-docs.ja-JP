---
title: このエディションで非推奨の API 要素
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: e40bcbfffc6f149837f4a11351f2bdbbf0dcc524
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571599"
---
# <a name="api-elements-deprecated-in-this-edition"></a>このエディションで非推奨の API 要素

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
Microsoft Outlook 2013 では、次の API 要素は推奨されていません。 サポートされていませんし、新しいプロジェクトで使用する必要がありません。
  
## <a name="deprecation-of-message-and-recipient-options"></a>メッセージと受信者のオプションの廃止

次の API 要素は古いメッセージと受信者のオプションこのリリースでは使用されなくなりました。
  
- **IXPLogon::RegisterOptions**など、MAPI サブシステムが不要になったトランスポート プロバイダーのメッセージと受信者のオプションの既定値を確立するためには、このメソッドを呼び出します。
    
- **OPTIONDATA**- と受信者のメッセージのオプションのプロパティがサポートされているこのデータ構造体は使用されていません。 MAPI サブシステムには、不要になった任意のメッセージまたはトランスポート プロバイダーは、特定のアドレスの種類をサポートしている受信者のオプションを取得するのには**IXPLogon::RegisterOptions**が呼び出されます。 
    
- **OPTIONCALLBACK**: この関数のプロトタイプ、トランスポート プロバイダーを使用して、コールバック関数をさらに、宣言、プロバイダーのプロパティを解決するのには使用する MAPI サブシステムが古くなった。 **IXPLogon::RegisterOptions**やトランスポート プロバイダーによって返されるすべてのコールバック関数を使用して、MAPI サブシステムが不要になった。 
    
- **IMAPISession::MessageOptions**: MAPI クライアントとサービスのプロバイダーは、プロパティの表示または特定のメッセージとアドレスの種類を制御するプロパティを設定できるようにするには、このメソッドを呼び出す必要がありますできなくします。 メソッドは、常に、特定のメッセージのメッセージのオプションがないことを示す MAPI_E_NOT_FOUND を返します。
    
- **IMAPISession::QueryDefaultMessageOpt**: MAPI クライアントとサービスのプロバイダーは、特定のアドレスの種類をメッセージのオプションを制御するプロパティを取得するには、このメソッドを呼び出す必要がありますできなくします。 不要になったプロパティの値の配列へのポインターを返します。
    
- **IAddrBook::RecipOptions**: MAPI クライアントとサービスのプロバイダーは、プロパティの表示、またはユーザーがそのコントロールの処理を特定のアドレスの種類の受信者のプロパティを設定できるようにするには、このメソッドを呼び出す必要がありますできなくします。 メソッドは、特定の宛先の受信者のオプションがないことを示す、MAPI_W_ERRORS_RETURNED を常に返します。
    
- **IAddrBook::QueryDefaultRecipOpt**: MAPI クライアントとサービスのプロバイダーは、特定のアドレスの種類の受信者のオプションを制御するプロパティを取得するには、このメソッドを呼び出す必要がありますできなくします。 不要になったプロパティの値の配列へのポインターを返します。
    
## <a name="see-also"></a>関連項目



[Outlook MAPI リファレンスの概要](getting-started-with-the-outlook-mapi-reference.md)

