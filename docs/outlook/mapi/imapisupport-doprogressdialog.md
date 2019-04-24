---
title: imapisupportdo進捗ダイアログ
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3de29e9af5caa82d2e57c8fcbbdab7d5ddb19dd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285207"
---
# <a name="imapisupportdoprogressdialog"></a>IMAPISupport::DoProgressDialog

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
進行状況インジケーターを表示する progress オブジェクトを取得します。
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>パラメーター

 _uluiparam_
  
> 順番進行状況インジケーターの親ウィンドウへのハンドル。
    
 _ulFlags_
  
> 順番進捗状況オブジェクトが進捗状況を計算する方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_TOP_LEVEL 
  
> 最上位レベルのアイテム (親フォルダーなど) について、進行状況が計算されます。 progress オブジェクトは、imapiprogress の値を使用する必要があり[ます。:P rogress](imapiprogress-progress.md)メソッドの_ulcount_および_ulcount_パラメーター (それぞれ、現在のアイテムおよび操作の合計アイテムを示す) を使用して、進行状況を増分します。操作のインジケーター。 
    
 _lppprogress_
  
> 読み上げprogress オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> progress オブジェクトが正常に取得されました。
    
## <a name="remarks"></a>解説

**imapisupport::D o進捗ダイアログ**メソッドは、アドレス帳とメッセージストアプロバイダーのサポートオブジェクトに実装されています。 これらのプロバイダーは**doprogress ダイアログ**を呼び出して、進行状況の情報を計算し、標準ダイアログボックスを表示する[imapiprogress](imapiprogressiunknown.md)インターフェイスの MAPI 実装にアクセスします。 
  
progress オブジェクトと**imapiprogress**インターフェイスを使用する方法については、「[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[進行状況インジケーターを表示する](how-to-display-a-progress-indicator.md)

