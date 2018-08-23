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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 828d7ebcbceead02441165e3af92ec7b47d9f001
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564627"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ ・ ストア内のメッセージでは通常、オブジェクトの複合のエントリ id ストア内のオブジェクトのエントリ id とストアのエントリの識別子に ASCII 文字を分離します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
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
  
> [in]クライアント アプリケーションによって使用中のセッションへのポインター。 
    
 _szMsgID_
  
> [in]オブジェクトのエントリ id を表す文字列です。 
    
 _pcbStoreEID_
  
> [out]返されたサイズ (バイト)、オブジェクトを含むメッセージ ストアのエントリの識別子へのポインター。 普通のエントリの識別子に、 _szMsgID_パラメーターが指している場合は文字列、 _pcbStoreEID_パラメーターが指す 0 です。 
    
 _ppStoreEID_
  
> [out]オブジェクトを含むメッセージ ストアのエントリが返される識別子へのポインターへのポインター。 _SzMsgID_パラメーターは、普通のエントリの識別子をポイントしている場合、 _ppStoreEID_パラメーターに NULL が返されます。 
    
 _pcbMsgEID_
  
> [out]返されたサイズ (バイト)、そのストア内のオブジェクトのエントリ id へのポインター。 _SzMsgID_パラメーターは、普通のエントリの識別子の文字列をポイントしている場合、 _pcbMsgEID_パラメーターは、 _cbEID_パラメーターの値に等しい。 
    
 _ppMsgEID_
  
> [out]そのストア内のオブジェクトの返されるエントリの識別子の文字列へのポインターへのポインター。 _SzMsgID_パラメーターは、普通のエントリの識別子をポイントしている場合、 _ppMsgEID_は、普通のエントリ id の変換されたコピーへのポインターをポイントします。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

_SzMsgID_パラメーターで指定された識別子は、複合、ascii 変換し、メッセージ ・ ストア内のオブジェクトのエントリ id とストアのエントリ id を分割します。 単に普通のエントリの識別子の文字列が変換され、コピーされます。 複合識別子文字列が区切られている、通常は[HrComposeMsgID](hrcomposemsgid.md)関数によって作成されます。 
  
**HrDecomposeMsgID**関数の呼び出しは、 [HrEntryIDFromSz](hrentryidfromsz.md)関数とし、 [HrDecomposeEID](hrdecomposeeid.md)関数を呼び出すことと同じです。 
  

