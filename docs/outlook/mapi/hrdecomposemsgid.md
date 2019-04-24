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
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348091"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトの複合エントリ識別子 (通常はメッセージストア内のメッセージ) の ASCII 表記を、ストア内のそのオブジェクトのエントリ id、およびストアのエントリ識別子に分割します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
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
  
> 順番クライアントアプリケーションによって使用されているセッションへのポインター。 
    
 _szMsgID_
  
> 順番オブジェクトのエントリ id を表す文字列。 
    
 _pcbstoreeid_
  
> 読み上げオブジェクトを含むメッセージストアのエントリ id の、返されるサイズをバイト単位で示したポインターです。 _szMsgID_パラメーターが非複合エントリ識別子の文字列を指している場合、 _pcbstoreeid_パラメーターは0を指しています。 
    
 _ppstoreeid_
  
> 読み上げオブジェクトを含むメッセージストアの返されたエントリ id へのポインターへのポインター。 _szMsgID_パラメーターが非複合エントリ識別子を指している場合、 _ppstoreeid_パラメーターでは NULL が返されます。 
    
 _pcbmsgeid_
  
> 読み上げ格納されているオブジェクトのエントリ id の、返されるサイズ (バイト数) へのポインター。 _szMsgID_パラメーターが非複合エントリ識別子の文字列を指している場合、 _pcbmsgeid_パラメーターは_cbeid_パラメーターの値と等しくなります。 
    
 _ppmsgeid_
  
> 読み上げストア内でのオブジェクトの返されたエントリ識別子文字列へのポインターへのポインター。 _szMsgID_パラメーターが非複合エントリ識別子をポイントしている場合、 _ppmsgeid_は、非複合エントリ識別子の変換されたコピーへのポインターを指します。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>解説

_szMsgID_パラメーターによって指定された識別子が複合である場合、その識別子は ASCII から変換され、メッセージストア内のオブジェクトのエントリ id とストアのエントリ識別子に分割されます。 非複合エントリ識別子の文字列は単に変換およびコピーされます。 複合識別子の文字列は、通常、 [HrComposeMsgID](hrcomposemsgid.md)関数によって作成されたものです。 
  
**HrDecomposeMsgID**関数の呼び出しは、 [HrEntryIDFromSz](hrentryidfromsz.md)関数と[HrDecomposeEID](hrdecomposeeid.md)関数を呼び出すのと同じです。 
  

