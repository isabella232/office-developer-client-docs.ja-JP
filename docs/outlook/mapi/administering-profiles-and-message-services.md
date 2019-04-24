---
title: プロファイルとメッセージサービスを管理する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1e64241008a4adde4431b2c9683199294f21e396
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330234"
---
# <a name="administering-profiles-and-message-services"></a>プロファイルとメッセージサービスを管理する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルとメッセージサービスの管理には、新しいプロファイルを作成したり、古いプロファイルを削除したり、既存のプロファイルの内容を変更したりすることが含まれます。その中に含まれるメッセージサービスとサービスプロバイダーを変更します。 すべてのクライアントが、プロファイルとメッセージサービスの管理を標準的な機能としてサポートするわけではありません。 クライアントによっては、ユーザーがログオン時に1つを選択できるというよりもプロファイルを使用することができません。
  
プロファイルまたはメッセージサービスの管理をサポートしている場合は、MAPI で実装されている次のインターフェイスを使用する可能性があります。
  
- [IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)を使用して、プロファイル内のメッセージサービスを管理します。 [imapisession:: adminservices](imapisession-adminservices.md)または[IProfAdmin:: adminservices](iprofadmin-adminservices.md)のどちらかを通じてアクセスできます。 メッセージングクライアントは、通常、構成クライアント、またはメッセージの送受信が行われないクライアントの間に**imapisession**を呼び出します。 **IProfAdmin**を呼び出します。 可能な限り、 **IProfAdmin**メソッドを呼び出すと、メッセージサービスは開始されません。 **IMsgServiceAdmin**インターフェイスの使用方法の詳細については、「message service の[構成](configuring-a-message-service.md)」、「[メッセージサービスのコピー](copying-a-message-service.md)」、および「[メッセージサービスの削除](deleting-a-message-service.md)」を参照してください。
    
- [IProfAdmin:](iprofadminiunknown.md) [MAPIAdminProfiles](mapiadminprofiles.md)関数を通じてアクセスできる、プロファイルを管理する IUnknown。 **IProfAdmin**インターフェイスの使用の詳細については、以下のトピックを参照してください。[カスタムコードを使用したプロファイルの作成](creating-a-profile-by-using-custom-code.md)、プロファイルの[コピー](copying-a-profile.md)、プロファイルの[削除](deleting-a-profile.md)、[プロファイル名の検索](finding-a-profile-name.md)、および[の設定既定のプロファイル](setting-a-default-profile.md)。
    
- [IProfSect: imapiprop](iprofsectimapiprop.md)を使用して、プロファイルセクションのプロパティを維持します。これには、 [imapiprop:: openprofile](imapisession-openprofilesection.md)または[IProviderAdmin:: openprofile](iprovideradmin-openprofilesection.md)のセクションメソッドを通じてアクセスできます。 プロファイルセクションの詳細については、「 [MAPI プロファイル](mapi-profiles.md)」を参照してください。
    
- [IProviderAdmin: IUnknown](iprovideradminiunknown.md)を使用して、メッセージサービスのサービスプロバイダーを管理します。 [IMsgServiceAdmin:: adminproviders](imsgserviceadmin-adminproviders.md)を通じてアクセスできます。 **IProviderAdmin**インターフェイスの使用の詳細については、「[メッセージサービスでプロバイダーを追加または削除](adding-or-deleting-providers-in-a-message-service.md)する」を参照してください。
    
プロファイルとメッセージサービスの管理のサポートに注意してください。 使用されているプロファイルの悪影響から保護する対策はありません。 MAPI を使用すると、使用中のプロファイルを削除することはできませんが、すべてのメッセージサービスを削除することはできません。 プロファイル内のすべてのメッセージサービスを削除すると、これらのサービスのすべてのサービスプロバイダーが停止し、予期しない結果が発生する原因になります。
  
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
    
[メッセージサービスを追加する](adding-a-message-service.md)
  
> メッセージサービスを追加する方法について説明します。
    
[メッセージサービスの構成](configuring-a-message-service.md)
  
> メッセージサービスを構成する方法について説明します。
    
[メッセージサービスのコピー](copying-a-message-service.md)
  
> メッセージサービスをプロファイルにコピーする方法について説明します。
    
[メッセージサービスの削除](deleting-a-message-service.md)
  
> メッセージサービスを削除する方法について説明します。
    
[メッセージサービスでのプロバイダーの追加または削除](adding-or-deleting-providers-in-a-message-service.md)
  
> メッセージサービスでプロバイダーを追加または削除する方法について説明します。
    

