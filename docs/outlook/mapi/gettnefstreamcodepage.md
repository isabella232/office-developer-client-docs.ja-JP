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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399656"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート ニュートラル カプセル化形式 (TNEF) ストリームのコード ページを決定します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |tnef.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス ・ プロバイダーです。  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>パラメーター

 _lpStream_
  
> [in]TNEF ストリーム メッセージのソースを提供するストレージ ストリーム オブジェクト OLE の**IStream**インターフェイスへのポインター。 
    
 _lpulCodepage_
  
> [out]ストリームのコード ページへのポインター。
    
 _lpulSubCodepage_
  
> [out]ストリームのサブコードのページへのポインター。
    
## <a name="return-value"></a>戻り値

 **S_OK**
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> TNEF ストリーム内の属性を読み取り中にエラーが発生しました。
    
 **MAPI_E_CORRUPT_DATA**
  
> ストリームが TNEF ストリームではないか、attOemCodepage 属性を読み取り中にエラーが発生しました。
    
## <a name="remarks"></a>備考

TNEF ストリームのコード ページとサブコードのページを決定するのにの**attOemCodepage**属性を読み取ることには、 **GetTnefStreamCodepage**関数を使用します。 **AttOemCodepage**が見つからない場合、 **GetTnefStreamCodepage**は、コード ページ 437 と 0 のサブコードのページを返します。 
  
## <a name="see-also"></a>関連項目



[attOemCodepage](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

