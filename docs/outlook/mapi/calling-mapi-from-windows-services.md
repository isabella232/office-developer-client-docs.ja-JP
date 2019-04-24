---
title: Windows サービスからの MAPI の呼び出し
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
# <a name="calling-mapi-from-windows-services"></a>Windows サービスからの MAPI の呼び出し

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi 準拠のサービスプロバイダーで動作するように Windows サービスとして記述されている mapi クライアントアプリケーションを有効にするために、mapi にはいくつかの制限と要件があります。
  
MAPI クライアントには、次の制限があります。
  
- ユーザーインターフェイスを許可することはできません。
    
- メッセージは密結合されたメッセージストアとトランスポートプロバイダーを使用してのみ送信できます。 また、MAPI クライアントは、Microsoft Exchange Server または別のサーバーベースのトランスポートプロバイダーのみを使用して、メッセージの送受信を行うことができます。 クライアントアプリケーションと MAPI スプーラーとの間の id とセキュリティの問題のため、サービスではほとんどのトランスポートプロバイダーがサポートされていません。 
    
Windows サービスとして実装されているかどうかにかかわらず、すべての mapi クライアントアプリケーションは、 [MAPIInitialize](mapiinitialize.md)関数を呼び出して mapi ライブラリを初期化する必要があります。 [oleinitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx)関数の呼び出しは、OLE ライブラリを使用するためにも必要です。 [MAPIInitialize](mapiinitialize.md)と[oleinitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx)の両方で、 [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx)関数を呼び出して、コンポーネントオブジェクトモデル (COM) ライブラリを初期化します。 サービスであるクライアントは、 [MAPIInitialize](mapiinitialize.md)に渡される[MAPIINIT_0](mapiinit_0.md)構造の**ulflags**メンバーと、 [MAPILogonEx](mapilogonex.md)に渡される_ulflags_パラメーターに、特殊なフラグ MAPI_NT_SERVICE を設定する必要があります。MAPI に特別な実装を通知する関数。 
  
Windows サービスとして記述され、mapi クライアントインターフェイスで記述された mapi クライアントには、追加の要件があります。 MAPI_NO_MAIL フラグは、 [MAPILogonEx](mapilogonex.md)への呼び出しで設定する必要があります。 他の種類のクライアントは、MAPI によって自動的に設定されるので、ログオンのフラグを設定する必要はありません。
  
初期化スレッドでメッセージを処理するために、サービスとして実装されている MAPI クライアントは次のことを行います。
  
1. メインスレッドがブロックされたときに[MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx)関数を呼び出します。 
    
2. [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx)、 [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)、および[DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx)の一連の Windows 関数を呼び出して、 [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx)が_nCount_パラメーターの値の合計を返す場合にメッセージを処理します。**WAIT_OBJECT_0**の値。これは、メッセージがキューにあることを示します。
    
## <a name="see-also"></a>関連項目



[MAPIInitialize](mapiinitialize.md)
  
[MAPIINIT_0](mapiinit_0.md)
  
[MAPILogonEx](mapilogonex.md)


[操作環境の問題](operating-environment-issues.md)

