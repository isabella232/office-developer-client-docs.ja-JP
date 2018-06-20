---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c4859fa4f8f55af7913c884e25c96727c063ba79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800165"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**適用されます**: Outlook 
  
トランスポート ニュートラル カプセル化形式 (TNEF) ストリームのコード ページを決定します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |tnef.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダーです。  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>Parameters

 _lpStream_
  
> [in]TNEF ストリーム メッセージのソースを提供するストレージ ストリーム オブジェクト OLE の**IStream**インターフェイスへのポインター。 
    
 _lpulCodepage_
  
> [out]ストリームのコード ページへのポインター。
    
 _lpulSubCodepage_
  
> [out]ストリームのサブコードのページへのポインター。
    
## <a name="return-value"></a>�߂�l

 **S_OK**
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> TNEF ストリーム内の属性を読み取り中にエラーが発生しました。
    
 **MAPI_E_CORRUPT_DATA**
  
> ストリームが TNEF ストリームではないか、attOemCodepage 属性を読み取り中にエラーが発生しました。
    
## <a name="remarks"></a>備考

TNEF ストリームのコード ページとサブコードのページを決定するのにの**attOemCodepage**属性を読み取ることには、 **GetTnefStreamCodepage**関数を使用します。 **AttOemCodepage**が見つからない場合、 **GetTnefStreamCodepage**は、コード ページ 437 と 0 のサブコードのページを返します。 
  
## <a name="see-also"></a>関連項目



[attOemCodepage](http://msdn.microsoft.com/en-us/library/ee158667%28EXCHG.80%29.aspx)

