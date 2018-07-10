---
title: プロファイルとメッセージ サービスの管理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 71e8cf50c1951abf1df6163cae4757ffebc979b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799647"
---
# <a name="administering-profiles-and-message-services"></a>プロファイルとメッセージ サービスの管理

  
  
**適用されます**: Outlook 
  
プロファイルとメッセージのサービスの管理は、新しいプロファイルを作成する、古いプロファイルを削除して、メッセージ サービス、およびそれらに含まれているサービス ・ プロバイダーを変更することで既存のプロファイルの内容を変更することを含めることができます。 すべてのクライアントは、標準的な機能としてのプロファイルとメッセージ サービスの管理をサポートします。 一部のクライアントがある以外のユーザーは、ログオン時にいずれかの選択を許可するよりも、プロファイルを使用して操作を行います。
  
プロファイル、またはメッセージ サービスの管理をサポートする場合可能性は、次の MAPI によって実装されるインターフェイスを使用します。
  
- [IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) [IMAPISession::AdminServices](imapisession-adminservices.md)または[IProfAdmin::AdminServices](iprofadmin-adminservices.md)のいずれかを介してアクセスできるように、プロファイル内のメッセージ サービスを管理します。 メッセージング クライアントは、通常の構成のクライアント、またはクライアントの操作を行いますしない送信またはメッセージが表示される、 **IProfAdmin**を呼び出しているときに**IMAPISession**を呼び出します。 、可能な限りは、メッセージ サービスを開始するのには行われませんので、 **IProfAdmin**メソッドを呼び出します。 詳細については、 **IMsgServiceAdmin**インターフェイスを使用して、次のトピックを参照してください:[メッセージ サービスを構成する](configuring-a-message-service.md)、[メッセージ サービスのコピー](copying-a-message-service.md)、および[メッセージ サービスを削除](deleting-a-message-service.md)します。
    
- [IProfAdmin: IUnknown](iprofadminiunknown.md)プロファイル、 [MAPIAdminProfiles](mapiadminprofiles.md)関数を使用してアクセスを管理します。 詳細については、 **IProfAdmin**インターフェイスを使用して、次のトピックを参照してください:[カスタム コードを使用してプロファイルを作成する](creating-a-profile-by-using-custom-code.md)[プロファイルをコピーする](copying-a-profile.md)[プロファイルの削除](deleting-a-profile.md)、[プロファイル名の検索](finding-a-profile-name.md)、および[の設定、既定のプロファイル](setting-a-default-profile.md)。
    
- [IProfSect: IMAPIProp](iprofsectimapiprop.md) 、 [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)または[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md)メソッドを使用してアクセスのプロファイル セクションでプロパティを維持するためにします。 プロファイル セクションの詳細については、 [MAPI プロファイル](mapi-profiles.md)を参照してください。
    
- [IProviderAdmin: IUnknown](iprovideradminiunknown.md) [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)経由でアクセスできる、メッセージ サービスのサービス プロバイダーを管理します。 詳細については、 **IProviderAdmin**インターフェイスを使用して、[追加、またはメッセージ サービスのプロバイダーを削除する](adding-or-deleting-providers-in-a-message-service.md)を参照してください。
    
プロファイルとメッセージ サービスの管理のサポートに注意が必要であります。 悪影響が使用されているプロファイルの変更から保護する保護機能はありません。 MAPI は、使用中のプロファイルを削除してからを防ぐことができますが、内のすべてのメッセージ サービスを削除するを防ぐことはできません。 プロファイル内のすべてのメッセージ サービスを削除すると、すべてのこれらのサービスのサービス プロバイダーが原因となり、発生する予期しない結果が停止します。
  
## <a name="in-this-section"></a>このセクションの内容

[プロファイルを作成します。](creating-a-profile.md)
  
> プロファイルを作成する方法について説明します。
    
[プロファイルをコピーします。](copying-a-profile.md)
  
> プロファイルをコピーする方法について説明します。
    
[プロファイルを削除します。](deleting-a-profile.md)
  
> プロファイルを削除する方法について説明します。
    
[既定のプロファイルを設定します。](setting-a-default-profile.md)
  
> 既定のプロファイルを設定する方法について説明します。
    
[プロファイル名の検索](finding-a-profile-name.md)
  
> プロファイルの名前を検索する方法について説明します。
    
[メッセージ サービスを追加します。](adding-a-message-service.md)
  
> メッセージ サービスを追加する方法について説明します。
    
[メッセージ サービスを構成します。](configuring-a-message-service.md)
  
> メッセージ サービスを構成する方法について説明します。
    
[メッセージ サービスのコピー](copying-a-message-service.md)
  
> メッセージ サービスをプロファイルにコピーする方法について説明します。
    
[メッセージ サービスを削除します。](deleting-a-message-service.md)
  
> メッセージ サービスを削除する方法について説明します。
    
[追加するか、メッセージ サービスのプロバイダーを削除します。](adding-or-deleting-providers-in-a-message-service.md)
  
> メッセージ サービス内のプロバイダーを追加、削除する方法について説明します。
    
