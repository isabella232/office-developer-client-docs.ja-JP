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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351129"
---
# <a name="imapiviewcontextgetsavestream"></a>IMAPIViewContext::GetSaveStream

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のメッセージを保存するために使用するストリームを取得します。
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a>パラメーター

 _/フラグ_
  
> 読み上げメッセージテキストの保存方法を制御するフラグのビットマスクへのポインター。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> メッセージテキストは、Unicode 形式で保存されます。 MAPI_UNICODE フラグが設定されていない場合、テキストは ANSI 形式で保存されます。
    
 _指定形式_
  
> 読み上げ保存されたテキストの形式を制御するフラグのビットマスクへのポインター。 次のフラグを設定できます。
    
SAVE_FORMAT_RICHTEXT 
  
> メッセージテキストは、リッチテキスト形式 (RTF) で書式設定されたテキストとして保存されます。 
    
SAVE_FORMAT_TEXT 
  
> メッセージテキストは、プレーンテキストとして保存されます。 
    
 _ppstm_
  
> 読み上げ保存されたメッセージを格納するストリームへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ストリームが正常に取得されました。
    
## <a name="remarks"></a>解説

form オブジェクトは、 **imapiviewcontext:: GetSaveStream**メソッドを呼び出して、フォームビューアーでの [名前を付けて保存の操作をサポートする**IStream**インターフェイスを実装するオブジェクトをストリームを取得します。 [imapiform::D overb](imapiform-doverb.md)メソッドは、フォームサーバーに実装され、動詞を呼び出すためにフォームビューアーによって呼び出されます。メッセージが完全に適切なテキスト形式に変換され、適切なストリームに配置されるまで、戻りません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**GetSaveStream**を呼び出す前に、 _ppstm_が指すストリームに書き込みを行わないでください。 **GetSaveStream**が返された場合、シークポインターの位置をリセットしません。 このポインターは、保存されたメッセージテキストの末尾に置いておく必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

