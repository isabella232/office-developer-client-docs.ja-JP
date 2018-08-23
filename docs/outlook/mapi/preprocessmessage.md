---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 878c3aaf22a6cf8a08c8234df41b671088c435c7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584990"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージの内容またはメッセージの形式を指定する関数を定義します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|によって実装される関数の定義:  <br/> |トランスポート プロバイダー  <br/> |
|によって呼び出される関数を定義します。  <br/> |MAPI スプーラー  <br/> |
   
```cpp
HRESULT PreprocessMessage(
  LPVOID lpvSession,
  LPMESSAGE lpMessage,
  LPADRBOOK lpAdrBook,
  LPMAPIFOLDER lpFolder,
  LPALLOCATEBUFFER AllocateBuffer,
  LPALLOCATEMORE AllocateMore,
  LPFREEBUFFER FreeBuffer,
  ULONG FAR * lpcOutbound,
  LPMESSAGE FAR * FAR * lpppMessage,
  LPADRLIST FAR * lppRecipList
);
```

## <a name="parameters"></a>パラメーター

 _lpvSession_
  
> [in]使用するセッションへのポインター。 
    
 _lpMessage_
  
> [in]前処理が必要にメッセージへのポインター。 
    
 _lpAdrBook_
  
> [in]ユーザーがメッセージの受信者を選択する必要があります、アドレス帳へのポインター。 
    
 _lpFolder_
  
> [で [チェック アウト]フォルダーへのポインター。 入力では、 _lpFolder_のパラメーターは、前処理が必要にメッセージを含むフォルダーにポイントです。 出力では、 _lpFolder_は、プリプロセス済みのメッセージが設定されているフォルダーをポイントします。 
    
 _lpAllocateBuffer_
  
> [in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpAllocateMore_
  
> [in]追加メモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインターに必要な場所です。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _lpcOutbound_
  
> [out]_LpppMessage_パラメーターが指す配列内のメッセージの数へのポインターです。 
    
 _lpppMessage_
  
> [out]ポインターの配列へのポインターへのポインターでは、前処理またはそれ以外の場合にメッセージを生成します。 
    
 _lppRecipList_
  
> [out]オプションへのポインターには、メッセージが配信できなかった、プリプロセッサが検出された受信者を一覧表示、 [ADRLIST](adrlist.md)構造体が返されます。 このリストの内容の詳細については、 [IMAPISupport::StatusRecips](imapisupport-statusrecips.md)メソッドを参照してください。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> メッセージの内容は、正常にプリプロセス済みでした。
    
## <a name="remarks"></a>注釈

メッセージ トランスポート プロバイダー プリプロセッサでは、メッセージのプリプロセス中に進行状況のインジケーターを表示できます。 ただし、メッセージのプリプロセス中にユーザーとの対話を必要とするダイアログ ボックスが表示されない必要があります。 
  
プリプロセッサでは、大量のデータを送信メッセージに追加するときは、特定の手順を行ってください。 この種類のメッセージは、時間のかかる処理をリモート ストアにアクセスするのにはプリプロセッサの原因で、サーバー ベースのメッセージ ・ ストアに格納できます。 これを行うことを避けるためには、プリプロセッサの大量の領域は、ローカル メッセージ ストアのデータを格納し、メッセージのローカル ストアへの参照を提供することを可能にするオプションが必要です。 
  
プリプロセッサは最初**PreprocessMessage**ベースの関数に渡されたオブジェクトのいずれかを開放しなければなりません。 
  
MAPI スプーラーは、 **PreprocessMessage**関数を呼び出すことができます、前にトランスポート プロバイダーは、必要がありますに登録されている関数、 [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md)メソッドを呼び出す。 **PreprocessMessage**関数を呼び出すと、関数が戻るまでにメッセージを送信する、スプーラーを続行できません。 
  
MAPI スプーラーは、メッセージを送信するタスクを所有しています。 これは、元のメッセージがメッセージのポインターの配列に配置されることはありませんし、 **SubmitMessage**メソッドの呼び出しが必要ではないことを意味します。 
  
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

