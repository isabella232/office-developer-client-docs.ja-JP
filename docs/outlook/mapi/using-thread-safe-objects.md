---
title: オブジェクトThread-Safe使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 418eb34ee6b66a941a32bc3e4dd7af29965d32c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590885"
---
# <a name="using-thread-safe-objects"></a>オブジェクトThread-Safe使用

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションでは、次の場合を除き、直接またはコールバックとして使用されるオブジェクトは常にスレッド セーフと見なされます。
  
- プロバイダーの状態テーブル行からのエントリ識別子を持つ [IMAPISession::OpenEntry](imapisession-openentry.md) へのクライアント呼び出しを通じて取得されたトランスポート プロバイダーの状態オブジェクト。 
    
- [MAPIOpenFormMgr](mapiopenformmgr.md)へのクライアント呼び出しを通じて取得された MAPI フォーム オブジェクトすべてです。 フォーム オブジェクトはアパートメント モデルルールに従い、クライアントはそれらを使用し、それらを作成したスレッドにのみ含まれるすべてのオブジェクトを使用する必要があります。
    
クライアントが、関連付けられた状態オブジェクトのエントリ識別子を含む状態テーブル内のトランスポート プロバイダーの行にアクセスすると、クライアントは、そのエントリ識別子を使用して **OpenEntry** を呼び出して、状態オブジェクトを開きます。 トランスポート プロバイダーは MAPI スプーラーのコンテキストで実行され、状態オブジェクトの個別のコンテキストを維持しないので、この状態オブジェクトはスレッド セーフではありません。 status オブジェクトはアパートメント モデル ルールに従い、クライアントはアパートメント モデルルールを作成したスレッドでのみ使用する必要があります。 
  
クライアントは、MAPI オブジェクトを使用する前に、すべてのスレッドで [MAPIInitialize](mapiinitialize.md) を呼び出し、その使用が完了したら [MAPIUninitialize](mapiuninitialize.md) を呼び出す必要があります。 これらの呼び出しは、使用するオブジェクトが外部ソースからスレッドに渡される場合でも行う必要があります。 **MAPIInitialize** および **MAPIUninitialize** は、Win32 **DllMain** 関数、プロセスとスレッドが初期化および終了するときにシステムによって呼び出される関数、 **または LoadLibrary** 関数と **FreeLibrary** 関数の呼び出し時以外の任意の場所から呼び出すことができます。 
  
間接使用オブジェクトは、スレッド セーフと見なす必要があります。 間接使用オブジェクトは、入力パラメーターとして宛先インターフェイス ポインターを必要とするメソッドによって返されます。 このようなメソッドの例は **、IMAPIProp::CopyTo** と CopyProps、IMAPIFolder::CopyFolder と **CopyMessage、****および IMsgServiceAdmin::CopyMsgService** です。  サービス プロバイダーが、渡されたスレッド以外のスレッドからそのようなオブジェクトを呼び出す場合、プロバイダーはオブジェクトを明示的にマーシャリングします。
  

