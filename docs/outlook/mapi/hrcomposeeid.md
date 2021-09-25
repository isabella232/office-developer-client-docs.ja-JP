---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ad7152106faaf604f2ea5306fce894a7117a06fa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584557"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトの複合エントリ識別子 (通常はメッセージ ストア内のメッセージ) を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
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
  
> [in]クライアント アプリケーションで使用されているセッションへのポインター。 
    
 _cbStoreRecordKey_
  
> [in]メッセージまたは他のオブジェクトを保持するメッセージ ストアのレコード キーのサイズ (バイト単位)。 _cbStoreRecordKey_ パラメーターに 0 が渡された場合 _、ppEID_ パラメーターはオブジェクトのエントリ識別子のコピーをポイントします。 
    
 _pStoreRecordKey_
  
> [in]メッセージまたは他のオブジェクトを含むメッセージ ストアのレコード キーへのポインター。 
    
 _cbMsgEID_
  
> [in]メッセージまたは他のオブジェクトのエントリ識別子のサイズ (バイト単位)。 
    
 _pMsgEID_
  
> [in]オブジェクトのエントリ識別子へのポインター。 
    
 _pcbEID_
  
> [out]返される識別子のサイズ (バイト単位) へのポインター。 
    
 _ppEID_
  
> [out]返されたエントリ識別子へのポインターを指すポインター。 _cbStoreRecordKey_ パラメーターの値が 0 より大きい場合 _、ppEID_ パラメーターは作成される複合エントリ識別子へのポインターを指します。 _cbStoreRecordKey が_ 0 の場合 _、ppEID_ はオブジェクトのエントリ識別子のコピーへのポインターを指します。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

複合エントリ識別子が作成されるメッセージまたは他のオブジェクトがメッセージ ストアに存在する場合、識別子はオブジェクトのエントリ識別子とストアのレコード キーから作成されます。 オブジェクトがストア内にない場合、つまり  _cbStoreRecordKey_ で渡されるストア レコード キーのバイト 数が 0 の場合、オブジェクトのエントリ識別子は単にコピーされます。 
  
**HrComposeEID 関数を使用** すると、アプリケーションは複合エントリ識別子を使用して複数のストア内のオブジェクトを操作できます。 アプリケーションは [、HrDecomposeEID](hrdecomposeeid.md) 関数を呼び出して、複合エントリ識別子を元の構成要素に分割できます。 
  
## <a name="see-also"></a>関連項目



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

