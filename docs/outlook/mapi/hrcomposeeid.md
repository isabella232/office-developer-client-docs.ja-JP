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
ms.openlocfilehash: 7de4fdefee67c79fb15ac28f821b015cdda6708d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348063"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクト (通常はメッセージストア内のメッセージ) の複合エントリ識別子を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
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
  
> 順番クライアントアプリケーションによって使用されているセッションへのポインター。 
    
 _cbStoreRecordKey_
  
> 順番メッセージまたはその他のオブジェクトを保持しているメッセージストアのレコードキーのサイズ (バイト数)。 _cbStoreRecordKey_パラメーターに0が渡された場合、 _ppeid_パラメーターはオブジェクトのエントリ識別子のコピーを指します。 
    
 _pStoreRecordKey_
  
> 順番メッセージまたはその他のオブジェクトを含むメッセージストアの record キーへのポインター。 
    
 _cbmsgeid_
  
> 順番メッセージまたはその他のオブジェクトのエントリ識別子のサイズ (バイト単位)。 
    
 _pmsgeid_
  
> 順番オブジェクトのエントリ識別子へのポインター。 
    
 _pcbeid_
  
> 読み上げ返される識別子のサイズ (バイト単位) へのポインター。 
    
 _ppeid_
  
> 読み上げ返されたエントリ識別子へのポインターへのポインター。 _cbStoreRecordKey_パラメーターの値が0より大きい場合、 _ppeid_パラメーターは作成された複合エントリ識別子へのポインターを指します。 _cbStoreRecordKey_が0の場合、 _ppeid_は、オブジェクトのエントリ識別子のコピーへのポインターを指します。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>解説

複合エントリ識別子が作成されているメッセージまたはその他のオブジェクトがメッセージストアに存在する場合は、そのオブジェクトのエントリ識別子とストアの record キーから識別子が作成されます。 オブジェクトがストアにない場合、つまり、 _cbStoreRecordKey_で渡されたストアレコードキーのバイト数が0の場合は、オブジェクトのエントリ識別子が単純にコピーされます。 
  
hrの参照**id**関数を使用すると、アプリケーションは複合エントリ識別子を使用して複数のストア内のオブジェクトを操作できます。 アプリケーションは[HrDecomposeEID](hrdecomposeeid.md)関数を呼び出して、複合エントリ識別子を元の constituents に分割できます。 
  
## <a name="see-also"></a>関連項目



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

