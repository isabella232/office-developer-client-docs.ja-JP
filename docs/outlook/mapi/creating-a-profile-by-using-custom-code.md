---
title: カスタム コードを使用したプロファイルの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f3270528194b3cc3429d3afec153355349dabbff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413305"
---
# <a name="creating-a-profile-by-using-custom-code"></a>カスタム コードを使用したプロファイルの作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルを作成するコードを作成する場合は、プロファイル エントリの注文方法と、各エントリに必要な情報の種類と量を理解してください。 プロファイル内のエントリを順序付けする場合の影響については [、「MAPI プロファイル」で説明します](mapi-profiles.md)。
  
 **C または C++ コードを使用してプロファイルを作成するには**
  
1. 各メッセージ サービスのヘッダー ファイルを読み取ります。 構成する必要があるプロパティと、使用する値を理解します。
    
2. [MAPIAdminProfiles 関数を呼び出](mapiadminprofiles.md)して **、IProfAdmin** インターフェイス ポインターを取得します。 
    
3. [IProfAdmin::CreateProfile](iprofadmin-createprofile.md)を呼び出してプロファイルを作成します。 MAPISVC の [既定のサービス] セクションに一覧表示されているメッセージ サービスを使用してプロファイルを作成する場合。INF ファイルで、フラグを設定MAPI_DEFAULT_SERVICEします。 ユーザーが構成情報を入力する場合は、このフラグをMAPI_DIALOGします。 MAPISVC を介して必要な情報の一部が利用できない場合は、必ずこのフラグを設定してください。INF ファイル。 **CreateProfile は** 、メッセージ サービスごとにエントリ ポイント関数を呼び出し  _、ulContext_ パラメーターとしてMSG_SERVICE_CREATEプロファイルに追加します。 
    
4. [IProfAdmin::AdminServices を呼び出](iprofadmin-adminservices.md)して、メッセージ サービス管理オブジェクトを取得します。 
    
5. メッセージ サービス管理オブジェクトを使用して、メッセージ サービスをプロファイルに追加します。 追加するメッセージ サービスごとに、次の処理を行います。
    
1. 新しい [メッセージ サービスを作成するには、IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) メソッドを呼び出します。 
    
2. [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出し、作成したサービスの **MAPIUID** 構造と、その構成プロパティを持つプロパティ値配列を渡します。 
    
6. PR_SERVICE_UID ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティである新しく追加されたサービスの識別子を取得するには[、IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)を呼び出してメッセージ サービス テーブルにアクセスし、メッセージ サービスを表す行を検索します。  表の最後の行は、最近追加されたメッセージ サービスを表します。 
    
新しいプロファイルを一時的に作成するには、ログオン直後に [IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md) メソッドを呼び出します。 **DeleteProfile は** 、新しいプロファイルを削除済みとしてマークし、セッションの期間中は使用できます。 セッションのプロファイル テーブルには含まれませんので、他のクライアントでは使用できません。 
  

