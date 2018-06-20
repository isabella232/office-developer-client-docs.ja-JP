---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e66d48b6caefe0fee67f41ea829db3201751cf27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800291"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**適用されます**: Outlook 
  
ストア内のオブジェクトのエントリ id とストアのエントリの識別子、メッセージ ・ ストア内のメッセージでは通常、オブジェクトの複合のエントリ id に分割します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
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

## <a name="parameters"></a>Parameters

 _psession_
  
> [in]クライアント アプリケーションによって使用中のセッションへのポインター。 
    
 _cbEID_
  
> [in]分離する複合エントリの識別子のバイト単位のサイズです。 
    
 _pEID_
  
> [in]分離する複合エントリの識別子へのポインター。 
    
 _pcbStoreEID_
  
> [out]返されたサイズ (バイト)、オブジェクトを含むメッセージ ストアのエントリの識別子へのポインター。 _PEID_パラメーターは、普通のエントリの識別子をポイントしている場合、 _pcbStoreEID_パラメーターが指す値が 0 の。 
    
 _ppStoreEID_
  
> [out]オブジェクトを含むメッセージ ストアのエントリが返される識別子へのポインターへのポインター。 _PEID_パラメーターは、普通のエントリの識別子をポイントしている場合、 _ppStoreEID_パラメーターに NULL が返されます。 
    
 _pcbMsgEID_
  
> [out]返されたサイズ (バイト)、オブジェクトのエントリの識別子へのポインター。 _PEID_パラメーターは、普通のエントリの識別子をポイントしている場合、 _pcbMsgEID_パラメーターは、 _cbEID_パラメーターの値に等しい。 
    
 _ppMsgEID_
  
> [out]オブジェクトの返されるエントリの識別子へのポインターへのポインター。 _PEID_パラメーターは、普通のエントリの識別子をポイントしている場合、 _ppMsgEID_は、普通のエントリ id のコピーへのポインターをポイントします。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>備考

_PEID_パラメーターで指定された識別子は、複合では、メッセージ ・ ストア内のオブジェクトのエントリ id とストアのエントリの識別子に分割されます。 普通のエントリの識別子の文字列がコピーされるだけです。 分離する複合識別子は、通常、 [HrComposeEID](hrcomposeeid.md)関数によって作成されたいずれかです。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_PEID_パラメーターを保持しているメモリは、この関数が正常に完了時に解放されます。 呼び出し元の実装では、出力パラメーター用のメモリを解放します。 
  

