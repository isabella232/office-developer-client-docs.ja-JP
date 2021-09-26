---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b8b1f2d590616a30464181bde9bb0d0ad989bb5a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610819"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトの複合エントリ識別子 (通常はメッセージ ストア内のメッセージ) を、ストア内のそのオブジェクトのエントリ識別子とストアのエントリ識別子に分離します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HrDecomposeEID(
  LPMAPISESSION psession,
  ULONG cbEID,
  LPENTRYID pEID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a>パラメーター

 _psession_
  
> [in]クライアント アプリケーションで使用されているセッションへのポインター。 
    
 _cbEID_
  
> [in]区切る複合エントリ識別子のサイズ (バイト単位)。 
    
 _pEID_
  
> [in]区切る複合エントリ識別子へのポインター。 
    
 _pcbStoreEID_
  
> [out]オブジェクトを含むメッセージ ストアのエントリ識別子の返されるサイズ (バイト単位) へのポインター。 _pEID パラメーターが_ 非コンパイルエントリ識別子をポイントする場合 _、pcbStoreEID_ パラメーターは値 0 をポイントします。 
    
 _ppStoreEID_
  
> [out]オブジェクトを含むメッセージ ストアの返されるエントリ識別子へのポインターへのポインター。 _pEID パラメーターが_ 非コンパイル エントリ識別子をポイントする場合 _、ppStoreEID_ パラメーターに NULL が返されます。 
    
 _pcbMsgEID_
  
> [out]オブジェクトのエントリ識別子の返されるサイズ (バイト単位) へのポインター。 _pEID パラメーター_ が非コンパイルエントリ識別子をポイントする場合 _、pcbMsgEID_ パラメーターは _cbEID_ パラメーターの値と等しくなります。 
    
 _ppMsgEID_
  
> [out]オブジェクトの返されたエントリ識別子へのポインターを指すポインター。 _pEID_ パラメーターが非コンパイルエントリ識別子を指している場合 _、ppMsgEID_ は非コンパイルエントリ識別子のコピーへのポインターを指します。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

_pEID_ パラメーターで指定された識別子が複合の場合、メッセージ ストア内のオブジェクトのエントリ識別子とストアのエントリ識別子に分割されます。 非compound エントリ識別子の文字列は、単にコピーされます。 区切る複合識別子は、通常 [、HrComposeEID 関数によって作成される識別子](hrcomposeeid.md) です。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_pEID_ パラメーターを保持するメモリは、この関数が正常に完了すると解放されます。 呼び出し元の実装は、出力パラメーターのメモリを解放します。 
  

