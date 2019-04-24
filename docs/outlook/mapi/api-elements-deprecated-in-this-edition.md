---
title: このエディションで廃止された API 要素
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: abfe734ad8af436f52fc0308d0cd236078bb47df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318209"
---
# <a name="api-elements-deprecated-in-this-edition"></a>このエディションで廃止された API 要素

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
次の API 要素は、Microsoft Outlook 2013 で廃止されました。 サポートされなくなったので、新しいプロジェクトで使用しないでください。
  
## <a name="deprecation-of-message-and-recipient-options"></a>メッセージと受信者のオプションの廃止

このリリースでは、次の API 要素が廃止されました。メッセージと受信者のオプションは、現在使用されていません。
  
- **IXPLogon:: registeroptions**— MAPI サブシステムは、このメソッドを呼び出して、トランスポートプロバイダーのメッセージおよび受信者オプションの既定値を設定することはできなくなりました。
    
- **optiondata**—メッセージおよび受信者オプションのプロパティをサポートするこのデータ構造は、現在は使用されていません。 MAPI サブシステムは、 **IXPLogon:: registeroptions**を呼び出して、トランスポートプロバイダーが特定のアドレスの種類に対してサポートしているメッセージまたは受信者オプションを取得することができなくなりました。 
    
- **optioncallback**-この関数プロトタイプは、コールバック関数を宣言するために使用され、さらに、プロバイダーのプロパティを解決するために使用される MAPI サブシステムは現在使われていません。 MAPI サブシステムは**IXPLogon:: registeroptions**を呼び出しません。または、トランスポートプロバイダーによって返されるコールバック関数を使用します。 
    
- **imapisession:: messageoptions**-MAPI クライアントおよびサービスプロバイダーは、このメソッドを呼び出してプロパティを表示したり、特定のメッセージおよびアドレスの種類を制御するプロパティをユーザーが設定したりすることはできなくなります。 メソッドは常に MAPI_E_NOT_FOUND を返します。これは、特定のメッセージにメッセージオプションがないことを示します。
    
- **imapisession:: querydefaultmessageopt**— MAPI クライアントおよびサービスプロバイダーは、特定のアドレスの種類のメッセージオプションを制御するプロパティを取得するために、このメソッドを呼び出すことができなくなります。 メソッドによって、プロパティ値の配列へのポインターが返されなくなりました。
    
- **IAddrBook:: RecipOptions**— MAPI クライアントおよびサービスプロバイダーは、このメソッドを呼び出してプロパティを表示したり、特定のアドレスの種類の受信者の処理を制御するプロパティをユーザーに設定したりすることができなくなります。 このメソッドは、常に MAPI_W_ERRORS_RETURNED を返します。この値は、特定の受信者に対して受信者のオプションが存在しないことを示します。
    
- **IAddrBook:: QueryDefaultRecipOpt**— MAPI クライアントおよびサービスプロバイダーは、特定のアドレスの種類の受信者オプションを制御するプロパティを取得するために、このメソッドを呼び出すことができなくなります。 メソッドによって、プロパティ値の配列へのポインターが返されなくなりました。
    
## <a name="see-also"></a>関連項目



[Outlook MAPI リファレンスの概要](getting-started-with-the-outlook-mapi-reference.md)

