---
title: このエディションで廃止された API 要素
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: ad61750e5b194859e4ed2b8963d017f3cabfb414
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588232"
---
# <a name="api-elements-deprecated-in-this-edition"></a>このエディションで廃止された API 要素

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
次の API 要素は、Microsoft Outlook 2013。 これらはサポートされなくなったので、新しいプロジェクトで使用する必要はありません。
  
## <a name="deprecation-of-message-and-recipient-options"></a>メッセージと受信者のオプションの廃止

このリリースでは、メッセージと受信者のオプションが廃止されたため、次の API 要素は廃止されました。
  
- **IXPLogon::RegisterOptions**—MAPI サブシステムは、トランスポート プロバイダーのメッセージおよび受信者オプションの既定値を確立するために、このメソッドを呼び出さなくなりました。
    
- **OPTIONDATA**:メッセージと受信者のオプションのプロパティをサポートしているこのデータ構造は使用されていません。 MAPI サブシステムは **、IXPLogon::RegisterOptions** を呼び出して、特定のアドレスの種類に対してトランスポート プロバイダーがサポートするメッセージまたは受信者オプションを取得しなくなりました。 
    
- **OPTIONCALLBACK**—この関数プロトタイプは、トランスポート プロバイダーがコールバック関数を宣言するために使用し、プロバイダーのプロパティの解決に使用される MAPI サブシステムは廃止されました。 MAPI サブシステムは **、IXPLogon::RegisterOptions** を呼び出したり、トランスポート プロバイダーから返されたコールバック関数を使用したりしなくなりました。 
    
- **IMAPISession::MessageOptions**—MAPI クライアントとサービス プロバイダーは、プロパティを表示したり、特定のメッセージとアドレスの種類を制御するプロパティを設定したりするために、このメソッドを呼び出さなくなりました。 メソッドは常にMAPI_E_NOT_FOUNDを返します。これは、特定のメッセージに対するメッセージ オプションが表示されません。
    
- **IMAPISession::QueryDefaultMessageOpt**—MAPI クライアントとサービス プロバイダーは、特定のアドレスの種類のメッセージ オプションを制御するプロパティを取得するために、このメソッドを呼び出さなくなりました。 メソッドは、プロパティ値の配列へのポインターを返しなくなりました。
    
- **IAddrBook::RecipOptions**—MAPI クライアントとサービス プロバイダーは、プロパティを表示したり、特定のアドレスの種類の受信者の処理を制御するプロパティを設定したりするために、このメソッドを呼び出さなくなりました。 メソッドは常にMAPI_W_ERRORS_RETURNEDを返します。これは、特定の受信者に対する受信者のオプションが表示されません。
    
- **IAddrBook::QueryDefaultRecipOpt**—MAPI クライアントとサービス プロバイダーは、特定のアドレスの種類の受信者オプションを制御するプロパティを取得するために、このメソッドを呼び出さなくなりました。 メソッドは、プロパティ値の配列へのポインターを返しなくなりました。
    
## <a name="see-also"></a>関連項目



[Outlook MAPI リファレンスの概要](getting-started-with-the-outlook-mapi-reference.md)

