---
title: MAPI を Windows サービスから呼び出す
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318107"
---
# <a name="calling-mapi-from-windows-services"></a>MAPI を Windows サービスから呼び出す

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI 準拠のサービス プロバイダーとWindows MAPI クライアント アプリケーションを有効にするには、MAPI にはいくつかの制限と要件が適用されます。
  
MAPI クライアントには、次の制限があります。
  
- ユーザー インターフェイスを許可することはできません。
    
- メッセージは、緊密に結合されたメッセージ ストアとトランスポート プロバイダーを介してのみ送信できます。 さらに、MAPI クライアントは、サーバーまたは別のサーバー ベースのトランスポート プロバイダー Microsoft Exchange Serverを使用してメッセージを送受信できます。 クライアント アプリケーションと MAPI スプーラー間の ID とセキュリティの問題のため、ほとんどのトランスポート プロバイダーはサービスではサポートされていません。 
    
MAPI クライアント アプリケーションは、すべての MAPI クライアント アプリケーションWindows、MAPI ライブラリを初期化するために[MAPIInitialize](mapiinitialize.md)関数を呼び出す必要があります。 OLE ライブラリを [使用するには、OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) 関数の呼び出しも必要です。 [MAPIInitialize と](mapiinitialize.md) [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx)の両方が[CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx)関数を呼び出して、コンポーネント オブジェクト モデル (COM) ライブラリを初期化します。 サービスであるクライアントは [、MAPIInitialize](mapiinitialize.md)に渡される [MAPIINIT_0](mapiinit_0.md)構造体の **ulFlags** メンバーと [、MAPILogonEx](mapilogonex.md)関数に渡される _ulFlags_ パラメーターに特別なフラグ MAPI_NT_SERVICE を設定して、MAPI に特別な実装を通知する必要があります。 
  
MAPI クライアント は、サービスWindows、MAPI クライアント インターフェイスで書き込まれる場合は、追加の要件を満たします。 MAPILogonEx の呼び出MAPI_NO_MAILフラグを設定 [する必要があります](mapilogonex.md)。 他の種類のクライアントは、MAPI によって自動的に設定されますので、ログオン用のフラグを設定する必要があります。
  
初期化スレッド内のメッセージを処理するために、サービスとして実装される MAPI クライアントは次の処理を行います。
  
1. メイン スレッド [がブロックされている場合は、MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) 関数を呼び出します。 
    
2. [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx)が nCount パラメーターの値と WAIT_OBJECT_0 の値の合計を返す場合に、メッセージを処理するために、Windows 関数の[GetMessage、TranslateMessage、](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx)および[DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx)シーケンスを呼び出します。これは、メッセージがキュー内にあるかどうかを示します。 [](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx) 
    
## <a name="see-also"></a>関連項目



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[オペレーティング環境の問題](operating-environment-issues.md)

