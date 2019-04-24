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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348070"
---
# <a name="hrdecomposeeid"></a>HrDecomposeEID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトの複合エントリ識別子 (通常はメッセージストア内のメッセージ) を、ストア内のそのオブジェクトのエントリ id、およびストアのエントリ識別子に分割します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
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
  
> 順番クライアントアプリケーションによって使用されているセッションへのポインター。 
    
 _cbeid_
  
> 順番分離する複合エントリ識別子のサイズ (バイト単位)。 
    
 _peid_
  
> 順番分離する複合エントリ識別子へのポインター。 
    
 _pcbstoreeid_
  
> 読み上げオブジェクトを含むメッセージストアのエントリ id の、返されるサイズをバイト単位で示したポインターです。 _peid_パラメーターが非複合エントリ識別子を指している場合、 _pcbstoreeid_パラメーターは0の値を指しています。 
    
 _ppstoreeid_
  
> 読み上げオブジェクトを含むメッセージストアの返されたエントリ id へのポインターへのポインター。 _peid_パラメーターが非複合エントリ識別子を指している場合、 _ppstoreeid_パラメーターでは NULL が返されます。 
    
 _pcbmsgeid_
  
> 読み上げオブジェクトのエントリ識別子のバイト単位で返されたサイズへのポインター。 _peid_パラメーターが非複合エントリ識別子を指している場合、 _pcbmsgeid_パラメーターは_cbeid_パラメーターの値と等しくなります。 
    
 _ppmsgeid_
  
> 読み上げオブジェクトの返されたエントリ識別子へのポインターへのポインター。 _peid_パラメーターが非複合エントリ識別子を指している場合、 _ppmsgeid_は非複合エントリ識別子のコピーへのポインターを指します。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>解説

_peid_パラメーターで指定された識別子が複合である場合、その id はメッセージストア内のオブジェクトのエントリ id とストアのエントリ識別子に分割されます。 非複合エントリ識別子の文字列は単にコピーされます。 分離する複合識別子は通常、hrの " [id](hrcomposeeid.md) " 関数で作成されたものです。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_peid_パラメーターを保持するメモリは、この関数が正常に完了した時点で解放されます。 呼び出し側の実装は、出力パラメーターのメモリを解放する役割を担います。 
  

