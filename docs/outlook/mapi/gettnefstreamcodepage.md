---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299434"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
カプセル化形式 (TNEF) ストリームTransport-Neutralコード ページを決定します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |tnef.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー。  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>パラメーター

 _lpStream_
  
> [in]TNEF ストリーム メッセージのソースを提供するストレージ ストリーム オブジェクト OLE **IStream** インターフェイスへのポインター。 
    
 _lpulCodepage_
  
> [out]ストリームのコード ページへのポインター。
    
 _lpulSubCodepage_
  
> [out]ストリームのサブコード ページへのポインター。
    
## <a name="return-value"></a>戻り値

 **S_OK**
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> TNEF ストリームで属性を読み取るエラーが発生しました。
    
 **MAPI_E_CORRUPT_DATA**
  
> ストリームが TNEF ストリームでなかったか、attOemCodepage 属性の読み取りエラーが発生しました。
    
## <a name="remarks"></a>注釈

**GetTnefStreamCodepage** 関数を使用して、TNEF ストリームの **attOemCodepage** 属性を読み取り、コード ページとサブコード ページを決定します。 **attOemCodepage** が見つからない場合 **、GetTnefStreamCodepage** は 437 のコード ページと 0 のサブコード ページを返します。 
  
## <a name="see-also"></a>関連項目



[attOemCodepage](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

