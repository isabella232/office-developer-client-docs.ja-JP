---
title: Windows サービスからの MAPI 呼び出し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385579"
---
# <a name="calling-mapi-from-windows-services"></a>Windows サービスからの MAPI 呼び出し

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI に準拠したサービス ・ プロバイダーで動作する Windows サービスとして記述されている MAPI クライアント アプリケーションを有効にするには、MAPI には、いくつかの制限事項と要件が課されます。
  
MAPI クライアントでは、次の制限があります。
  
- ユーザー インターフェイスすることができません。
    
- 密結合のメッセージ ・ ストアおよびトランスポート経由でのみメッセージを送信するプロバイダーです。 さらに、MAPI クライアントは送信し、Microsoft Exchange Server ではのみ、または別のサーバ ・ ベースのトランスポート プロバイダーを使用してメッセージを受信できます。 ほとんどのトランスポート プロバイダーは、クライアント アプリケーションと MAPI スプーラーとの間の id およびセキュリティの問題のため、サービスでサポートされていません。 
    
すべての MAPI クライアント アプリケーション、Windows サービスとして実装されるかどうかが MAPI ライブラリを初期化するために[生じます](mapiinitialize.md)関数を呼び出す必要があります。 [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx)関数の呼び出しは、OLE ライブラリを使用する必要もあります。 [生じます](mapiinitialize.md)、 [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx)の両方は、コンポーネント オブジェクト モデル (COM) ライブラリを初期化するために、 [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx)関数への呼び出しを確認します。 サービスのクライアント、MAPI_NT_SERVICE、特別なフラグ、 **ulFlags** 、 [MAPIINIT_0](mapiinit_0.md)構造体のメンバー[生じます](mapiinitialize.md)に渡されるのと設定[MAPILogonEx](mapilogonex.md)に渡される_ulFlags_パラメーターでMAPI の特殊な実装に通知する関数です。 
  
Windows サービスとして作成され、MAPI クライアント ・ インタ フェースを記述する MAPI クライアントでは、追加の要件があります。 [MAPILogonEx](mapilogonex.md)の呼び出しでは、MAPI_NO_MAIL フラグを設定する必要があります。 その他の種類のクライアントは、MAPI によって自動的に設定されているために、ログオンにフラグを設定する必要はありません。
  
初期化スレッドでメッセージを処理するためにサービスとして実装されている MAPI クライアントは、次の。
  
1. [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx)関数を呼び出すときに、メイン スレッドはブロックします。 
    
2. _NCount_パラメーターの値の合計が[MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx)に返されるときにメッセージを処理するために Windows の機能の[自動インクリメント](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx)を[獲得](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)で[もないとき](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx)のシーケンスを呼び出すと、**WAIT_OBJECT_0**メッセージがキュー内であることを示す値です。
    
## <a name="see-also"></a>関連項目



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[操作環境の問題](operating-environment-issues.md)

