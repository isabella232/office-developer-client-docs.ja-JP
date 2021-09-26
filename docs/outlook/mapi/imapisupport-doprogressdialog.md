---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2941178a46b6cd1323d3ccb8ffe3acd97f631155
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620892"
---
# <a name="imapisupportdoprogressdialog"></a>IMAPISupport::DoProgressDialog

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
進行状況インジケーターを表示する進行状況オブジェクトを取得します。
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]進行状況インジケーターの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> [in]進行状況オブジェクトが進行状況を計算する方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_TOP_LEVEL 
  
> 進行状況は、親フォルダーなどの上位レベルのアイテムに対して計算されます。 progress オブジェクトは、操作の進行状況インジケーターをインクリメントするために [、IMAPIProgress::P rogress](imapiprogress-progress.md) メソッドの  _ulCount_ パラメーターと  _ulTotal_ パラメーターの値を使用する必要があります。 
    
 _lppProgress_
  
> [out]progress オブジェクトへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> progress オブジェクトが正常に取得されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::D oProgressDialog** メソッドは、アドレス帳およびメッセージ ストア プロバイダーのサポート オブジェクトに実装されます。 これらのプロバイダーは **DoProgressDialog** を呼び出して [IMAPIProgress](imapiprogressiunknown.md) インターフェイスの MAPI 実装にアクセスし、進行状況情報を計算し、標準のダイアログ ボックスを表示します。 
  
進行状況オブジェクトと **IMAPIProgress** インターフェイスを使用する方法については、「進捗インジケーターを表示 [する」を参照してください](how-to-display-a-progress-indicator.md)。
  
## <a name="see-also"></a>関連項目



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)

