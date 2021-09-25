---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 32988bc25e32ec3350a6e58e6418130a31f2095b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580189"
---
# <a name="getattribimsgonistg"></a>GetAttribIMsgOnIStg

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[OpenIMsgOnIStg](openimsgonistg.md)関数によって指定された[IMessage](imessageimapiprop.md)オブジェクトのプロパティの属性を取得します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Imessage.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとメッセージ ストア プロバイダー  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a>パラメーター

 _lpObject_
  
> [in][OpenIMsgOnIStg](openimsgonistg.md)関数から取得した **IMessage** オブジェクトへのポインター。 
    
 _lpPropTagArray_
  
> [in]取得する属性のプロパティを示すプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。 
    
 _lppPropAttrArray_
  
> [out]取得したプロパティ属性を含む [、返される SPropAttrArray](spropattrarray.md) 構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは全体的に成功しましたが、1 つ以上のプロパティにアクセスする必要が生じ、プロパティの種類が変更されたPT_ERROR。
    
## <a name="remarks"></a>注釈

プロパティ属性にアクセスできるのは、プロパティ オブジェクト、つまり [IMAPIProp : IUnknown](imapipropiunknown.md) インターフェイスを実装するオブジェクトのみです。 OLE 構造化ストレージ オブジェクトで MAPI プロパティを使用するために [、OpenIMsgOnIStg](openimsgonistg.md)は OLE **IStorage** オブジェクトの上に [IMessage : IMAPIProp](imessageimapiprop.md)オブジェクトを作成します。 このようなオブジェクトのプロパティ属性は [、SetAttribIMsgOnIStg](setattribimsgonistg.md) を使用して設定または変更し **、GetAttribIMsgOnIStg** を使用して取得できます。 
  
> [!NOTE]
> **GetAttribIMsgOnIStg** および **SetAttribIMsgOnIStg** は、すべての **IMessage オブジェクトで動作しません** 。 これらは **、OpenIMsgOnIStg** によって返される **IMessage**-on- **IStorage** オブジェクトでのみ有効です。 
  
_lppPropAttrArray_ パラメーター内の属性の数と位置は _、lpPropTagArray_ パラメーター内のプロパティ タグの数と位置に対応します。 
  

