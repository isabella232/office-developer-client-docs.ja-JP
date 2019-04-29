---
title: スレッドセーフオブジェクトの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 611e0a49f0fd8df8fe40205a33ed5501055c3d45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425170"
---
# <a name="using-thread-safe-objects"></a>スレッドセーフオブジェクトの使用

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントアプリケーションは、次の場合を除き、直接またはコールバックとして使用されているオブジェクトが常にスレッドセーフであることを前提としています。
  
- クライアント呼び出しによって取得された、 [imapisession:: openentry](imapisession-openentry.md)をプロバイダーの状態テーブルの行からのエントリ識別子を使用して取得した、トランスポートプロバイダーの状態オブジェクト。 
    
- クライアントから[MAPIOpenFormMgr](mapiopenformmgr.md)への呼び出しによって取得されたすべての MAPI フォームオブジェクト。 フォームオブジェクトはアパートメントモデルルールに従い、クライアントはそれらを使用する必要があります。また、これらのオブジェクトは、それらを作成したスレッドにのみ含まれます。
    
クライアントは、関連付けられている状態オブジェクトのエントリ識別子を含む状態テーブル内のトランスポートプロバイダーの行にアクセスすると、そのエントリ識別子を持つ**openentry**を呼び出して status オブジェクトを開くことができます。 この状態オブジェクトはスレッドセーフではありません。トランスポートプロバイダーは MAPI スプーラーのコンテキストで実行され、状態オブジェクトに対して個別のコンテキストを維持しないため、スレッドセーフではありません。 status オブジェクトは、アパートメントモデルルールに従い、クライアントはそれを作成したスレッドでのみ使用する必要があります。 
  
また、クライアントは、すべてのスレッドで[MAPIInitialize](mapiinitialize.md)を起動してから、その使用が完了したときに MAPI オブジェクトおよび[MAPIUninitialize](mapiuninitialize.md)を使用する必要があります。 これらの呼び出しは、使用するオブジェクトが外部ソースからスレッドに渡される場合でも実行する必要があります。 **MAPIInitialize**および**MAPIUninitialize**は、Win32 **DllMain**関数内から、プロセスとスレッドが初期化および終了されるときにシステムによって呼び出される関数、またはその**他の場所から呼び出すことができます。LoadLibrary**関数と**FreeLibrary**関数 
  
Indirect use オブジェクトは、スレッドセーフと見なされないようにする必要があります。 間接使用オブジェクトは、入力パラメーターとして宛先インターフェイスポインターを必要とするメソッドによって返されます。 このようなメソッドの例としては、 **imapiprop:: CopyTo**と**copyprops**、 **imapiprop:: copyprops**および**copyprops**、 **IMsgServiceAdmin:: copymsgservice**があります。 サービスプロバイダーが、渡されたスレッド以外のスレッドからこのようなオブジェクトを呼び出す場合、プロバイダーはオブジェクトを明示的にマーシャリングする必要があります。
  

