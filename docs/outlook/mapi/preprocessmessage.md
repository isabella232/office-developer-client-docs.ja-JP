---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 00d2dce81ecb8db1cd69406136b306acc731cc6c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550205"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの内容またはメッセージの形式を前処理する関数を定義します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|定義された関数は、次の方法で実装されます。  <br/> |トランスポート プロバイダー  <br/> |
|によって呼び出される定義済み関数:  <br/> |MAPI スプーラー  <br/> |
   
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
  
> [in]前処理するメッセージへのポインター。 
    
 _lpAdrBook_
  
> [in]ユーザーがメッセージの受信者を選択するアドレス帳へのポインター。 
    
 _lpFolder_
  
> [in, out]フォルダーへのポインター。 入力時に  _、lpFolder_ パラメーターは、前処理するメッセージを含むフォルダーをポイントします。 出力時に  _、lpFolder は_ 、前処理されたメッセージが配置されたフォルダーをポイントします。 
    
 _lpAllocateBuffer_
  
> [in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。 
    
 _lpAllocateMore_
  
> [in]必要に応じて追加のメモリを割り当てるのに使用する [MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。 
    
 _lpcOutbound_
  
> [out]  _lpppMessage_ パラメーターが指す配列内のメッセージ数へのポインター。 
    
 _lpppMessage_
  
> [out]プリプロセスまたはそれ以外の方法で生成されたメッセージへのポインターの配列へのポインター。 
    
 _lppRecipList_
  
> [out]メッセージが配信不能であるプリプロセッサが検出した受信者を一覧する、オプションで返される [ADRLIST](adrlist.md) 構造体へのポインター。 このリストの内容の詳細については [、「IMAPISupport::StatusRecips メソッド」を参照](imapisupport-statusrecips.md) してください。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> メッセージの内容が正常に前処理されました。
    
## <a name="remarks"></a>注釈

トランスポート プロバイダー のメッセージ プリプロセッサは、メッセージの前処理中に進行状況インジケーターを表示できます。 ただし、メッセージの前処理中にユーザー操作を必要とするダイアログ ボックスは表示されません。 
  
プリプロセッサが大量のデータを送信メッセージに追加する場合は、特定の手順に従う必要があります。 この種類のメッセージはサーバー ベースのメッセージ ストアに格納できます。これにより、プリプロセッサはリモート ストアにアクセスします。時間のかかる手順です。 これを避けるために、プリプロセッサには、ローカル メッセージ ストアに大量の領域を取るデータを格納し、メッセージ内のローカル ストアへの参照を提供できるオプションが必要です。 
  
プリプロセッサは **、PreprocessMessage** ベースの関数に最初に渡されたオブジェクトを解放しません。 
  
MAPI スプーラーが **PreprocessMessage** 関数を呼び出す前に、トランスポート プロバイダーは [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) メソッドの呼び出しで関数を登録している必要があります。 **PreprocessMessage 関数を呼び出** した後、スプーラーは、関数が返されるまでメッセージの送信を続行できません。 
  
MAPI スプーラーは、メッセージを送信するタスクを所有します。 つまり、元のメッセージはメッセージ ポインターの配列に配置されません **。SubmitMessage** メソッドの呼び出しは必要ありません。 
  
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

