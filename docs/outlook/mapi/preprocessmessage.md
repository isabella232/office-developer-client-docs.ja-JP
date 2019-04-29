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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437246"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの内容またはメッセージの形式を前にする関数を定義します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi  <br/> |
|定義された関数の実装:  <br/> |トランスポートプロバイダー  <br/> |
|によって呼び出された定義済み関数:  <br/> |MAPI スプーラー  <br/> |
   
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

 _lpvsession_
  
> 順番使用するセッションへのポインター。 
    
 _lpmessage_
  
> 順番前処理するメッセージへのポインター。 
    
 _lpadrbook_
  
> 順番ユーザーがメッセージの受信者を選択する必要があるアドレス帳へのポインター。 
    
 _lpfolder_
  
> [入力]フォルダーへのポインター。 入力時に_lpfolder_パラメーターは、前処理するメッセージを含むフォルダーを指します。 出力時に、 _lpfolder_はプリプロセスされたメッセージが配置されたフォルダーを指します。 
    
 _lpAllocateBuffer_
  
> 順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpAllocateMore_
  
> 順番必要なときに追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
 _lpfreebuffer_
  
> 順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _lpcOutbound_
  
> 読み上げ_lpppMessage_パラメーターによって指定された配列内のメッセージ数へのポインター。 
    
 _lpppMessage_
  
> 読み上げプリプロセスされた、または生成されたメッセージへのポインターの配列へのポインターへのポインター。 
    
 _lppRecipList_
  
> 読み上げメッセージが配信できない、プリプロセッサが検出された受信者を一覧表示する、オプションで返される[adrlist](adrlist.md)構造体へのポインター。 このリストの内容の詳細については、 [imapisupport:: StatusRecips](imapisupport-statusrecips.md)メソッドを参照してください。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> メッセージの内容が正常に前処理されました。
    
## <a name="remarks"></a>注釈

トランスポートプロバイダメッセージプリプロセッサは、メッセージの前処理中に進行状況インジケーターを表示できます。 ただし、メッセージ前処理中のユーザー操作を必要とするダイアログボックスを表示する必要はありません。 
  
プリプロセッサが送信メッセージに大量のデータを追加するときは、特定の手順に従う必要があります。 この種のメッセージをサーバーベースのメッセージストアに格納することにより、プリプロセッサがリモートストアにアクセスします。時間がかかるプロシージャです。 これを回避するために、プリプロセッサには、ローカルメッセージストアで大量の領域を必要とするデータを格納し、メッセージにそのローカルストアへの参照を提供できるオプションが用意されている必要があります。 
  
プリプロセッサは、元の**PreprocessMessage**ベースの関数に渡されたオブジェクトを解放してはなりません。 
  
MAPI スプーラーで**PreprocessMessage**関数を呼び出せるようにするには、トランスポートプロバイダーが[imapisupport:: registerpreprocessor プロセッサ](imapisupport-registerpreprocessor.md)メソッドへの呼び出しに関数を登録している必要があります。 **PreprocessMessage**関数を呼び出した後、スプーラーは、関数が戻るまで、メッセージの送信を続行できません。 
  
MAPI スプーラーは、メッセージを送信するタスクを所有しています。 これは、元のメッセージがメッセージポインターの配列に配置されることはないため、 **submitmessage**メソッドへの呼び出しが必要になることはありません。 
  
## <a name="see-also"></a>関連項目



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

