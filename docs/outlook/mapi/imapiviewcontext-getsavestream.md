---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 68eb74f53d6cee4661c98604ec2ea37609e20ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408426"
---
# <a name="imapiviewcontextgetsavestream"></a>IMAPIViewContext::GetSaveStream

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のメッセージの保存に使用するストリームを取得します。
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a>パラメーター

 _pulFlags_
  
> [out]メッセージ テキストの保存方法を制御するフラグのビットマスクへのポインター。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> メッセージ テキストは Unicode 形式で保存されます。 このフラグMAPI_UNICODE設定されていない場合、テキストは ANSI 形式で保存されます。
    
 _pulFormat_
  
> [out]保存されたテキストの形式を制御するフラグのビットマスクへのポインター。 次のフラグを設定できます。
    
SAVE_FORMAT_RICHTEXT 
  
> メッセージ テキストは、リッチ テキスト形式 (RTF) に書式設定されたテキストとして保存されます。 
    
SAVE_FORMAT_TEXT 
  
> メッセージ テキストはプレーン テキストとして保存されます。 
    
 _ppstm_
  
> [out]保存されたメッセージを含むストリームへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ストリームが正常に取得されました。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは **IMAPIViewContext::GetSaveStream** メソッドを呼び出して **、フォーム** ビューアーで Save As 動詞の処理をサポートするために IStream インターフェイスを実装するオブジェクトをストリームで取得します。 フォーム サーバーに実装され、動詞を呼び出すフォーム ビューアーによって呼び出される [IMAPIForm::D oVerb](imapiform-doverb.md) メソッドは、メッセージが完全に適切なテキスト形式に変換され、適切なストリームに配置されるまで返す必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

GetSaveStream を呼び出す前に  _、ppstm_ が指す **ストリームに書き込む必要があります**。 **GetSaveStream が** 返される場合は、シーク ポインターの位置をリセットしない。 このポインターは、保存されたメッセージ テキストの末尾に残る必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

