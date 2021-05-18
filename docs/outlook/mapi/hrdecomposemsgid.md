---
title: HrDecomposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404436"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトの複合エントリ識別子 (通常はメッセージ ストア内のメッセージ) の ASCII 表記を、ストア内のそのオブジェクトのエントリ識別子とストアのエントリ識別子に分離します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HrDecomposeMsgID(
  LPMAPISESSION psession,
  LPSTR szMsgID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a>パラメーター

 _psession_
  
> [in]クライアント アプリケーションで使用されているセッションへのポインター。 
    
 _szMsgID_
  
> [in]オブジェクトのエントリ識別子を表す文字列。 
    
 _pcbStoreEID_
  
> [out]オブジェクトを含むメッセージ ストアのエントリ識別子の返されるサイズ (バイト単位) へのポインター。 _szMsgID_ パラメーターが非コンパイルエントリ識別子文字列をポイントする場合 _、pcbStoreEID_ パラメーターは 0 をポイントします。 
    
 _ppStoreEID_
  
> [out]オブジェクトを含むメッセージ ストアの返されるエントリ識別子へのポインターへのポインター。 _szMsgID_ パラメーターが非コンパイルエントリ識別子をポイントする場合 _、ppStoreEID_ パラメーターで NULL が返されます。 
    
 _pcbMsgEID_
  
> [out]ストア内のオブジェクトのエントリ識別子の返されるサイズ (バイト単位) へのポインター。 _szMsgID_ パラメーターが非コンパイルエントリ識別子文字列をポイントする場合 _、pcbMsgEID_ パラメーターは _cbEID_ パラメーターの値と等しくなります。 
    
 _ppMsgEID_
  
> [out]ストア内のオブジェクトの返されるエントリ識別子文字列へのポインターを指すポインター。 _szMsgID_ パラメーターが非コンパイルエントリ識別子を指している場合 _、ppMsgEID_ は非コンパイルエントリ識別子の変換されたコピーへのポインターを指します。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

_szMsgID_ パラメーターで指定された識別子が複合の場合、ASCII から変換され、メッセージ ストア内のオブジェクトのエントリ識別子とストアのエントリ識別子に分割されます。 非compound エントリ識別子の文字列は、単に変換され、コピーされます。 区切る複合識別子文字列は、通常 [、HrComposeMsgID](hrcomposemsgid.md) 関数によって作成される文字列です。 
  
**HrDecomposeMsgID** 関数を呼び出すのは [、HrEntryIDFromSz](hrentryidfromsz.md)関数を呼び出してから [HrDecomposeEID](hrdecomposeeid.md)関数を呼び出すのと同じです。 
  

