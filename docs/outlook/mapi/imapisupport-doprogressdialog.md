---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 527a7bb3201a4a6b1bc0807136bc88b80c189de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800752"
---
# <a name="imapisupportdoprogressdialog"></a>IMAPISupport::DoProgressDialog

  
  
**適用されます**: Outlook 
  
進行状況インジケーターを表示する進行中のオブジェクトを取得します。
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]オブジェクトの進行状況が進行状況を計算する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_TOP_LEVEL 
  
> 親フォルダーなどのトップレベルの項目の進行状況が計算されます。 進行中のオブジェクトは、 [IMAPIProgress::Progress](imapiprogress-progress.md)メソッドの_ulCount_および_ulTotal_パラメーターの値を使用する必要があります-現在の項目と、操作でアイテムの合計をそれぞれ指定する: 進行状況をインクリメントするのには操作のインジケーターです。 
    
 _lppProgress_
  
> [out]進行中のオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 進行中のオブジェクトが正常に取得しました。
    
## <a name="remarks"></a>備考

アドレス帳、メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::DoProgressDialog**メソッドを実装します。 これらのプロバイダーは、MAPI インターフェイスの実装、 [IMAPIProgress](imapiprogressiunknown.md) 、進捗状況の情報を計算し、標準のダイアログ ボックスを表示するにアクセスするために**DoProgressDialog**を呼び出します。 
  
進行中のオブジェクトと、 **IMAPIProgress**インターフェイスを使用する方法の詳細については、[進行状況のインジケーターの表示](how-to-display-a-progress-indicator.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIProgress: IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[進行状況インジケーターを表示します。](how-to-display-a-progress-indicator.md)
