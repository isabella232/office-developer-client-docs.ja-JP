---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419395"
---
# <a name="imapiviewcontextsetadvisesink"></a>IMAPIViewContext::SetAdviseSink

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームの登録を管理して、閲覧者の変更に関する通知を受信します。 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>パラメーター

 _pmvns_
  
> 順番フォームアドバイズシンクオブジェクトまたは NULL へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォーム通知の登録または取り消しに成功しました。
    
## <a name="remarks"></a>注釈

form オブジェクトは**imapiviewcontext:: SetAdviseSink**メソッドを呼び出して、フォームビューアーの変更について学習するか、前に登録を取り消します。 _pmvns_が NULL に設定されている場合、フォームは登録をキャンセルする必要があります。 _pmvns_が有効な form アドバイズシンクを指している場合、フォームは将来の通知の登録を希望します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**SetAdviseSink**にフォームアドバイズシンクポインターが含まれている場合は、別の**SetAdviseSink**呼び出しが行われてから、通知が取り消されるまで、そのポインターへの参照を保持します。 viewer で変更が発生したとき、および新しいメッセージを読み込むときに通知を送信します。 
  
詳細については、「[フォーム通知の送信と受信](sending-and-receiving-form-notifications.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer  <br/> |cmymapiformviewer:: SetAdviseSink  <br/> |mfcmapi は、この関数に**imapiviewcontext:: SetAdviseSink**メソッドを実装します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

