---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4d38648f5e3084c8342fca8d18f0bd3efc915155
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412633"
---
# <a name="imapifoldercreatemessage"></a>IMAPIFolder::CreateMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しいメッセージを作成します。
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a>パラメーター

 _lpinterface_
  
> 順番新しいメッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 有効なインターフェイス識別子には、IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、および IID_IMAPIFolder があります。 NULL を渡すと、メッセージストアプロバイダーは標準のメッセージインターフェイス[IMessage: imapiprop](imessageimapiprop.md)を返します。 
    
 _ulFlags_
  
> 順番メッセージの作成方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
ITEMPROC_FORCE
  
> ストアが新しいメッセージの到着をリッスンしているクライアントに通知する前に、そのメッセージがルール処理の対象となっていることを個人用フォルダーストア (PST) に示します。 ルール処理は、Microsoft exchange server 以外のサーバー上に作成された新しいメッセージにのみ適用されます。 exchange server は、サーバー上のメッセージのルールを処理するからです。 そのため、メッセージを作成するプロバイダーまたはクライアントは、 [IMAPIPProp:: SaveChanges](imapiprop-savechanges.md)を使用して、サーバーが Exchange サーバーではないことを示す NON_EMS_XP_SAVE を使用してメッセージを保存することにより、このフラグを渡す必要があります。 
    
MAPI_ASSOCIATED 
  
> 作成されるメッセージは、標準の contents テーブルではなく、関連付けられた contents テーブルに含まれている必要があります。 関連付けられたメッセージは、ユーザーの操作から非表示になります。
    
MAPI_DEFERRED_ERRORS 
  
> **CreateMessage**は、作成操作が完全に完了していない場合でも、成功することができます。 これは、新しいメッセージがすぐに発信者に対して使用できなくなる可能性があることを意味します。 
    
 _lppmessage_
  
> 読み上げ新しく作成されたメッセージへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージが正常に作成されました。
    
## <a name="remarks"></a>注釈

**imapifolder:: CreateMessage**メソッドは、標準または関連付けられたコンテンツを含む新しいメッセージを作成し、エントリ識別子を割り当てます。 エントリ識別子は、メッセージストアプロバイダーと個別のメッセージを表すパーツから構成されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**CreateMessage**ですべての必要なメッセージプロパティを設定するか、またはメッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドで設定するかを選択できます。 正常な保存が行われるまで、これらのプロパティを使用できないようにする必要はありません。 
  
関連情報の操作方法の詳細については、「[フォルダーに関連付けられた情報の表](folder-associated-information-tables.md)と内容」の[表](contents-tables.md)を参照してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

一部のメッセージストアプロバイダーでは、 **CreateMessage**が戻ると、すぐに新しいメッセージのエントリ識別子を使用できるようにすることができます。その他のメッセージストアプロバイダーは、メッセージが保存されるまで、可用性を遅らせます。 メッセージの**imapiprop:: SaveChanges**メソッドを呼び出しない限り、すべてのメッセージストアプロバイダーが新しいメッセージのエントリ識別子を生成しないため、 **CreateMessage**が戻るときに、エントリ id にアクセスできない場合があります。 また、新しいメッセージは、保存が行われるまでフォルダーの contents テーブルに含まれない場合があります。 
  
新しいメッセージに割り当てられたエントリ識別子は、現在のメッセージストアだけでなく、同時に開いているすべてのメッセージストアにわたって一意であると想定します。 このルールの1つの例外は、メッセージストアの複数のエントリがプロファイルに表示される場合に発生します。 これにより、メッセージストアが複数回開かれ、エントリ識別子が複製されます。 
  
送信メッセージを作成するには、送信トレイフォルダーの**imapifolder:: CreateMessage**メソッドを呼び出します。 
  
メッセージが保存される前に新しいメッセージを含むフォルダーを削除すると、結果は未定義となります。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|folderdlg  <br/> |cfolder:: onnewmessage  <br/> |mfcmapi は、 **imapifolder:: CreateMessage**メソッドを使用して、新しいメッセージを作成して保存します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

