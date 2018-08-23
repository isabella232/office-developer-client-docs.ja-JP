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
ms.openlocfilehash: f77b3dd9ca8c977574aab337b0df572404061b4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565866"
---
# <a name="calling-mapi-from-windows-services"></a>Windows サービスからの MAPI 呼び出し

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI に準拠したサービス ・ プロバイダーで動作する Windows サービスとして記述されている MAPI クライアント アプリケーションを有効にするには、MAPI には、いくつかの制限事項と要件が課されます。
  
MAPI クライアントでは、次の制限があります。
  
- ユーザー インターフェイスすることができません。
    
- 密結合のメッセージ ・ ストアおよびトランスポート経由でのみメッセージを送信するプロバイダーです。 さらに、MAPI クライアントは送信し、Microsoft Exchange Server ではのみ、または別のサーバ ・ ベースのトランスポート プロバイダーを使用してメッセージを受信できます。 ほとんどのトランスポート プロバイダーは、クライアント アプリケーションと MAPI スプーラーとの間の id およびセキュリティの問題のため、サービスでサポートされていません。 
    
すべての MAPI クライアント アプリケーション、Windows サービスとして実装されるかどうかが MAPI ライブラリを初期化するために[生じます](mapiinitialize.md)関数を呼び出す必要があります。 [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx)関数の呼び出しは、OLE ライブラリを使用する必要もあります。 [生じます](mapiinitialize.md)、 [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx)の両方は、コンポーネント オブジェクト モデル (COM) ライブラリを初期化するために、 [CoInitialize](http://msdn.microsoft.com/en-us/library/ms678543%28VS.85%29.aspx)関数への呼び出しを確認します。 サービスのクライアント、MAPI_NT_SERVICE、特別なフラグ、 **ulFlags** 、 [MAPIINIT_0](mapiinit_0.md)構造体のメンバー[生じます](mapiinitialize.md)に渡されるのと設定[MAPILogonEx](mapilogonex.md)に渡される_ulFlags_パラメーターでMAPI の特殊な実装に通知する関数です。 
  
Windows サービスとして作成され、MAPI クライアント ・ インタ フェースを記述する MAPI クライアントでは、追加の要件があります。 [MAPILogonEx](mapilogonex.md)の呼び出しでは、MAPI_NO_MAIL フラグを設定する必要があります。 その他の種類のクライアントは、MAPI によって自動的に設定されているために、ログオンにフラグを設定する必要はありません。
  
初期化スレッドでメッセージを処理するためにサービスとして実装されている MAPI クライアントは、次の。
  
1. [MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx)関数を呼び出すときに、メイン スレッドはブロックします。 
    
2. _NCount_パラメーターの値の合計が[MsgWaitForMultipleObjects](http://msdn.microsoft.com/en-us/library/ms684242%28VS.85%29.aspx)に返されるときにメッセージを処理するために Windows の機能の[自動インクリメント](http://msdn.microsoft.com/en-us/library/ms644936%28VS.85%29.aspx)を[獲得](http://msdn.microsoft.com/en-us/library/ms644955%28VS.85%29.aspx)で[もないとき](http://msdn.microsoft.com/en-us/library/ms644934%28VS.85%29.aspx)のシーケンスを呼び出すと、**WAIT_OBJECT_0**メッセージがキュー内であることを示す値です。
    
## <a name="see-also"></a>関連項目



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[操作環境の問題](operating-environment-issues.md)

