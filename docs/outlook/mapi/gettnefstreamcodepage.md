---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299434"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートに中立的なカプセル化形式 (TNEF) ストリームのコードページを指定します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |tnef  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー。  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>パラメーター

 _lpstream_
  
> 順番TNEF ストリームメッセージのソースを提供する、ストレージストリームオブジェクトの OLE **IStream**インターフェイスへのポインター。 
    
 _lアウトコードページ_
  
> 読み上げストリームのコードページへのポインター。
    
 _lアウト subcodepage_
  
> 読み上げストリームのサブコードページへのポインター。
    
## <a name="return-value"></a>戻り値

 **S_OK**
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> TNEF ストリームの属性の読み取り中にエラーが発生しました。
    
 **MAPI_E_CORRUPT_DATA**
  
> ストリームが TNEF ストリームではなかったか、attoemcodepage 属性の読み取り中にエラーが発生しました。
    
## <a name="remarks"></a>解説

**GetTnefStreamCodepage**関数を使用して、TNEF ストリームの**attoemcodepage**属性を読み取り、コードページとサブコードページを特定します。 **attoemcodepage**が見つからない場合、 **GetTnefStreamCodepage**は437のコードページとサブコードページを0に返します。 
  
## <a name="see-also"></a>関連項目



[attoemcodepage](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

