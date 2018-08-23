---
title: スレッド セーフ オブジェクトの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4a66f892043b9a90893a60f3fa6ba69ea6457f5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804223"
---
# <a name="using-thread-safe-objects"></a>スレッド セーフ オブジェクトの使用

  
  
**適用対象**: Outlook 
  
クライアント アプリケーションは、オブジェクトが直接使用されるか、コールバックとは、常にスレッド セーフである場合を除き以下のような場合を想定します。
  
- トランスポート プロバイダーの状態のオブジェクトがクライアントを呼び出すことによって[IMAPISession::OpenEntry](imapisession-openentry.md)のエントリ id を持つプロバイダーの状態のテーブルの行から取得します。 
    
- [MAPIOpenFormMgr](mapiopenformmgr.md)へのクライアント呼び出しによって取得されたすべての MAPI フォーム オブジェクト。 フォーム オブジェクトがアパートメント モデルの規則に従うし、それを作成したスレッド上でのみが含まれているすべてのオブジェクトとそのクライアントを使用する必要があります。
    
ステータスが関連付けられているオブジェクトのエントリ id を含むステータスの表に、トランスポート プロバイダーの行をクライアントにアクセスする場合、クライアントは、状態オブジェクトを開くには、そのエントリ id を持つ**OpenEntry**を呼び出すことができます。 トランスポート プロバイダーは、MAPI スプーラーのコンテキストで実行され、その状態のオブジェクトを別のコンテキストを保持しないために、この状態オブジェクトはスレッド セーフではありません。 状態オブジェクトがアパートメント モデルの規則に従うし、クライアントがそれを作成したスレッド上でのみ使用する必要があります。 
  
クライアントは[生じます](mapiinitialize.md)をその使用が完了したら、任意の MAPI オブジェクトと[MAPIUninitialize](mapiuninitialize.md)を使用する前にすべてのスレッドで呼び出しもする必要があります。 使用するオブジェクトが外部ソースからのスレッドに渡された場合でも、これらの呼び出しを行ってください。 **生じます**し、 **MAPIUninitialize**呼び出すことができますから任意の場所以外から Win32 **DllMain**関数の場合、システム プロセスやスレッドの初期化や終了、または、**への呼び出し時に呼び出される関数内でLoadLibrary**し**終わった**関数です。 
  
スレッド セーフにするオブジェクトの間接使用を前提としません。 間接使用オブジェクトは、入力パラメーターとしてインターフェイス ポインターの移動先を必要とするメソッドによって返されます。 このようなメソッドには、 **IMAPIProp::CopyTo**と**CopyProps**、 **IMAPIFolder::CopyFolder** **CopyMessage**、および**IMsgServiceAdmin::CopyMsgService**があります。 サービス プロバイダーが渡されましたが別のスレッドからこのようなオブジェクトを呼び出す場合は、プロバイダーは、明示的にオブジェクトをマーシャ リングします。
  

