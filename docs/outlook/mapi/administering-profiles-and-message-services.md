---
title: プロファイルとメッセージ サービスの管理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 238982026b61f8559560619e6c8dd76db291c9b3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564457"
---
# <a name="administering-profiles-and-message-services"></a>プロファイルとメッセージ サービスの管理

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルとメッセージ サービスの管理には、新しいプロファイルの作成、古いプロファイルの削除、および既存のプロファイルに含まれるメッセージ サービスとサービス プロバイダーの変更による既存のプロファイルの内容の変更が含まれる場合があります。 一部のクライアントがプロファイルとメッセージ サービスの管理を標準機能としてサポートしている場合ではありません。 一部のクライアントは、ユーザーがログオン時にプロファイルを選択できる以上の関係を持っていません。
  
プロファイルまたはメッセージ サービスの管理をサポートしている場合は、MAPI によって実装されている次のインターフェイスを使用する可能性があります。
  
- [IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) は [、IMAPISession::AdminServices](imapisession-adminservices.md) または [IProfAdmin::AdminServices](iprofadmin-adminservices.md)のいずれかを介してアクセスできるプロファイルでメッセージ サービスを管理します。 メッセージング クライアントは、通常 **、IMAPISession** を呼び出しますが、構成クライアント、またはメッセージを送受信しないクライアントは **、IProfAdmin を呼び出します**。 可能な限り、メッセージ サービスが開始されないので **、IProfAdmin** メソッドを呼び出します。 **IMsgServiceAdmin** インターフェイスの使用の詳細については、「メッセージ サービスの構成 [](configuring-a-message-service.md)、メッセージ サービスのコピー [](copying-a-message-service.md)、およびメッセージ サービスの削除」を [参照してください](deleting-a-message-service.md)。
    
- [IProfAdmin : MAPIAdminProfiles](iprofadminiunknown.md)関数からアクセスできるプロファイルを管理する[IUnknown。](mapiadminprofiles.md) **IProfAdmin** インターフェイスの使用の詳細については、「カスタム コードを使用 [](creating-a-profile-by-using-custom-code.md)したプロファイルの作成、プロファイルのコピー、プロファイルの削除、[](deleting-a-profile.md)プロファイル名の検索、[](finding-a-profile-name.md)および既定のプロファイルの設定 [](setting-a-default-profile.md)」を参照してください。 [](copying-a-profile.md)
    
- [IProfSect : IMAPIProp](iprofsectimapiprop.md) を使用して [、IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) メソッドまたは [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) メソッドからアクセスできる、プロファイル セクションのプロパティを維持します。 プロファイル セクションの詳細については [、「MAPI プロファイル」を参照してください](mapi-profiles.md)。
    
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md) は [、IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)を介してアクセス可能なメッセージ サービスでサービス プロバイダーを管理します。 **IProviderAdmin** インターフェイスの使用の詳細については、「メッセージ サービスでのプロバイダーの追加または削除」[を参照してください](adding-or-deleting-providers-in-a-message-service.md)。
    
プロファイルとメッセージ サービスの管理のサポートに注意してください。 使用されているプロファイルを悪影響を及ぼす変更から保護するための保護手段はありません。 MAPI では、使用されているプロファイルを削除することはできませんが、その中のすべてのメッセージ サービスを削除することはできません。 プロファイル内のすべてのメッセージ サービスを削除すると、これらのサービスのすべてのサービス プロバイダーが停止し、予期しない結果が発生します。
  
## <a name="in-this-section"></a>このセクションの内容

[プロファイルの作成](creating-a-profile.md)
  
> プロファイルを作成する方法について説明します。
    
[プロファイルのコピー](copying-a-profile.md)
  
> プロファイルをコピーする方法について説明します。
    
[プロファイルの削除](deleting-a-profile.md)
  
> プロファイルを削除する方法について説明します。
    
[既定のプロファイルの設定](setting-a-default-profile.md)
  
> 既定のプロファイルを設定する方法について説明します。
    
[プロファイル名の検索](finding-a-profile-name.md)
  
> プロファイルの名前を検索する方法について説明します。
    
[メッセージ サービスの追加](adding-a-message-service.md)
  
> メッセージ サービスを追加する方法について説明します。
    
[メッセージ サービスの構成](configuring-a-message-service.md)
  
> メッセージ サービスを構成する方法について説明します。
    
[メッセージ サービスのコピー](copying-a-message-service.md)
  
> メッセージ サービスをプロファイルにコピーする方法について説明します。
    
[メッセージ サービスの削除](deleting-a-message-service.md)
  
> メッセージ サービスを削除する方法について説明します。
    
[メッセージ サービスでのプロバイダーの追加または削除](adding-or-deleting-providers-in-a-message-service.md)
  
> メッセージ サービスでプロバイダーを追加または削除する方法について説明します。
    

