---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a9aa6deeca930da82db61ba517796bfbc0676467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800277"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**適用対象**: Outlook 
  
通常メッセージ ストア内のメッセージ オブジェクトは、複合のエントリの識別子を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HrComposeEID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  ULONG FAR * pcbEID,
  LPENTRYID FAR * ppEID
);
```

## <a name="parameters"></a>パラメーター

 _psession_
  
> [in]クライアント アプリケーションによって使用中のセッションへのポインター。 
    
 _cbStoreRecordKey_
  
> [in]メッセージまたはその他のオブジェクトを保持しているメッセージ ・ ストアのレコードのキーのバイト単位のサイズです。 _CbStoreRecordKey_パラメーターに 0 を渡した場合、 _ppEID_パラメーターは、オブジェクトのエントリ id のコピーを指します。 
    
 _pStoreRecordKey_
  
> [in]メッセージまたはその他のオブジェクトを含むメッセージ ストアのレコードのキーへのポインター。 
    
 _cbMsgEID_
  
> [in]メッセージまたはその他のオブジェクトのエントリ id のバイト単位のサイズです。 
    
 _pMsgEID_
  
> [in]オブジェクトのエントリの識別子へのポインター。 
    
 _pcbEID_
  
> [out]返される識別子のバイト単位のサイズへのポインター。 
    
 _ppEID_
  
> [out]返されるエントリの識別子へのポインターへのポインター。 _CbStoreRecordKey_パラメーターの値が 0 より大きい場合は、 _ppEID_パラメーターは、作成される複合エントリの識別子へのポインターを指します。 _CbStoreRecordKey_が 0 の場合は、 _ppEID_オブジェクトのエントリ id のコピーへのポインターが指します。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

メッセージ ストアでメッセージまたは複合のエントリの識別子を作成するための他のオブジェクトが存在する場合、識別子は、オブジェクトのエントリ id とストアのレコードのキーから作成されます。 オブジェクトがストア内にない場合は、 _cbStoreRecordKey_に渡されたストアのレコードのキーのバイト数が 0 の場合オブジェクトのエントリ id は単にコピーされます。 
  
**HrComposeEID**関数は、複合のエントリ id を使用して複数のストア内のオブジェクトを操作するアプリケーションを使用できます。 アプリケーションでは、複合のエントリの識別子を元の住民に分割する[HrDecomposeEID](hrdecomposeeid.md)関数を呼び出すことができます。 
  
## <a name="see-also"></a>関連項目



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

