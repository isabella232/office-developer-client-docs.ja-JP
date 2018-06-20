---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 418ffdd19412dcf948d36a5e7df33f7978d0df3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800276"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

  
  
**適用されます**: Outlook 
  
通常メッセージ ストア内のメッセージ オブジェクトは、複合のエントリの識別子を表す ASCII 文字列を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HrComposeMsgID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  LPSTR FAR * pszMsgID
);
```

## <a name="parameters"></a>Parameters

 _psession_
  
> [in]クライアント アプリケーションによって使用中のセッションへのポインター。 
    
 _cbStoreRecordKey_
  
> [in]メッセージまたはその他のオブジェクトを含むメッセージ ストアのレコードのキーのバイト単位のサイズです。 _CbStoreRecordKey_パラメーターに 0 を渡すと、エントリ id のコピーを_pszMsgID_のパラメーターのポイント テキストに変換します。 
    
 _pStoreRecordKey_
  
> [in]メッセージまたはその他のオブジェクトを含むメッセージ ストアのレコードのキーへのポインター。 
    
 _cbMsgEID_
  
> [in]メッセージまたはその他のオブジェクトのエントリ id のバイト単位のサイズです。 
    
 _pMsgEID_
  
> [in]オブジェクトのエントリの識別子へのポインター。 
    
 _pszMsgID_
  
> [out]返される ASCII 文字列へのポインター。 _CbStoreRecordKey_パラメーターが 0 より大きい場合は、複合のエントリの識別子に_pszMsgID_パラメーターのポイントは、テキストに変換します。 _CbStoreRecordKey_が 0 の場合は、普通のエントリの識別子に_pszMsgID_ポイントは、テキストに変換します。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>備考

メッセージ ストアでメッセージまたは複合のエントリの識別子を作成するための他のオブジェクトが存在する場合、識別子の文字列は、オブジェクトのエントリ id とストアのレコードのキーから作成されます。 オブジェクトがストア内にない場合は、 _cbStoreRecordKey_パラメーターで渡されたストアのレコードのキーのバイト数が 0 の場合オブジェクトのエントリ id は、単にコピーされ、文字列に変換します。 
  
**HrComposeMsgID**関数の呼び出しは、 [HrComposeEID](hrcomposeeid.md)関数とし、 [HrSzFromEntryID](hrszfromentryid.md)関数を呼び出すことと同じです。 
  
 **HrComposeMsgID**は、複合のエントリ id を使用して複数のストア内のオブジェクトを使用するクライアント アプリケーションを有効にします。 アプリケーションでは、複合のエントリの識別子を元の住民に分割する[HrDecomposeMsgID](hrdecomposemsgid.md)関数を呼び出すことができます。 
  

