---
title: ユーザー設定コードを使用したプロファイルの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c14d58e8a03633615798b50b256b9cc54fcc4f4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594734"
---
# <a name="creating-a-profile-by-using-custom-code"></a>ユーザー設定コードを使用したプロファイルの作成

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロファイルを作成するコードを記述することを選択する場合は、プロファイル エントリの種類と各エントリのために必要な情報の量を注文する方法を理解することを確認します。 プロファイル内のエントリの順序の影響は、 [MAPI プロファイル](mapi-profiles.md)で説明しています。
  
 **C または C++ のコードでプロファイルを作成するには**
  
1. 各メッセージ サービス用のヘッダー ファイルを参照します。 構成する必要がどのようなプロパティを理解し、使用しました。
    
2. **IProfAdmin**インターフェイス ポインターを取得するために[MAPIAdminProfiles](mapiadminprofiles.md)関数を呼び出します。 
    
3. プロファイルを作成するのには[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)を呼び出します。 場合、MAPISVC の **[サービスの既定値]** セクションに記載されているメッセージ サービスを使用してプロファイルを作成します。INF ファイルは、MAPI_DEFAULT_SERVICE フラグを設定します。 構成情報を入力するユーザーを有効にする場合は、MAPI_DIALOG フラグを設定します。 このフラグを設定するかどうかすべての必要な情報は、MAPISVC で利用できるようにしてください。INF ファイルです。 **CreateProfile**は、MSG_SERVICE_CREATE の_ulContext_のパラメーターとして設定すると、プロファイルに追加するには、各メッセージ サービスのエントリ ポイント関数を呼び出します。 
    
4. メッセージ サービス管理オブジェクトを取得する[IProfAdmin::AdminServices](iprofadmin-adminservices.md)を呼び出します。 
    
5. メッセージ サービスをプロファイルに追加するのにには、メッセージ サービスの管理オブジェクトを使用します。 メッセージ サービスごとに追加します。
    
1. 新しいメッセージ サービスを作成する[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドを呼び出します。 
    
2. [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)、作成したサービスの**MAPIUID**構造体とその構成のプロパティを持つプロパティ値の配列を渡すことを呼び出します。 
    
6. その**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティでは、新しく追加されたサービスの識別子を取得するために、メッセージ サービス テーブルを表す行の検索にアクセスする[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)を呼び出すメッセージ サービスです。 テーブルの最後の行は、最後に追加されたメッセージ サービスを表します。 
    
新しいプロファイルは、一時的なものには、ログオンした後にすぐに[IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md)メソッドを呼び出します。 **DeleteProfile**は、セッション中に使用するときに削除されると、新しいプロファイルをマークします。 していないため、セッションのプロファイル テーブルに、に他のクライアントはそれを使用することができません。 
  

