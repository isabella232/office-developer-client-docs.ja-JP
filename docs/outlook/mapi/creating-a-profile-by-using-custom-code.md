---
title: カスタムコードを使用してプロファイルを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f3270528194b3cc3429d3afec153355349dabbff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335791"
---
# <a name="creating-a-profile-by-using-custom-code"></a>カスタムコードを使用してプロファイルを作成する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルを作成するコードの記述を選択する場合は、プロファイルエントリの順序付け方法と、各エントリに必要な情報の種類と量を理解していることを確認してください。 プロファイル内のエントリの順序付けの影響については、「 [MAPI プロファイル](mapi-profiles.md)」で説明されています。
  
 **C または C++ コードでプロファイルを作成するには**
  
1. 各メッセージサービスのヘッダーファイルを読み取ります。 構成する必要があるプロパティと、使用する値について説明します。
    
2. [MAPIAdminProfiles](mapiadminprofiles.md)関数を呼び出して、 **IProfAdmin**インターフェイスポインターを取得します。 
    
3. [IProfAdmin:: createprofile](iprofadmin-createprofile.md)を呼び出して、プロファイルを作成します。 mapisvc.inf の **[Default services]** セクションに表示されているメッセージサービスを使用してプロファイルを作成する場合。INF ファイルで、MAPI_DEFAULT_SERVICE フラグを設定します。 ユーザーが構成情報を入力できるようにするには、MAPI_DIALOG フラグを設定します。 mapisvc.inf で必要な情報をすべて利用できない場合は、このフラグが設定されていることを確認してください。INF ファイル **createprofile**は、MSG_SERVICE_CREATE が_ulcontext_パラメーターとして設定されているプロファイルに、各メッセージサービスのエントリポイント関数を呼び出します。 
    
4. [IProfAdmin:: adminservices](iprofadmin-adminservices.md)を呼び出して、メッセージサービス管理オブジェクトを取得します。 
    
5. メッセージサービスの管理オブジェクトを使用して、メッセージサービスをプロファイルに追加します。 追加するメッセージサービスごとに、次のように入力します。
    
1. [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)メソッドを呼び出して、新しいメッセージサービスを作成します。 
    
2. [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出して、作成したばかりのサービスの**MAPIUID**構造と、構成プロパティを持つプロパティ値配列を渡します。 
    
6. 新しく追加されたサービスの識別子 ( **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティ) を取得するには、 [IMsgServiceAdmin:: getmsgservicetable](imsgserviceadmin-getmsgservicetable.md)を呼び出してメッセージサービステーブルにアクセスし、次の行を表す行を検索します。メッセージサービス。 表の最後の行は、最近追加されたメッセージサービスを表します。 
    
新しいプロファイル一時を作成するには、ログオンした直後に[IProfAdmin::D eleteprofile](iprofadmin-deleteprofile.md)メソッドを呼び出します。 **deleteprofile**は、新しいプロファイルを削除済みとしてマークし、セッションの間は使用できるようにします。 これはセッションのプロファイルテーブルに含まれないため、他のクライアントはそれを使用できません。 
  

