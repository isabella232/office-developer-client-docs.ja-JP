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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c035780d3d790d94551860a418401e63da1c2151
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424064"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトの複合エントリ識別子 (通常はメッセージ ストア内のメッセージ) を表す ASCII 文字列を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
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

## <a name="parameters"></a>パラメーター

 _psession_
  
> [in]クライアント アプリケーションで使用されているセッションへのポインター。 
    
 _cbStoreRecordKey_
  
> [in]メッセージまたは他のオブジェクトを含むメッセージ ストアのレコード キーのサイズ (バイト単位)。 _cbStoreRecordKey_ パラメーターにゼロが渡された場合 _、pszMsgID_ パラメーターはテキストに変換されたエントリ識別子のコピーをポイントします。 
    
 _pStoreRecordKey_
  
> [in]メッセージまたは他のオブジェクトを含むメッセージ ストアのレコード キーへのポインター。 
    
 _cbMsgEID_
  
> [in]メッセージまたは他のオブジェクトのエントリ識別子のサイズ (バイト単位)。 
    
 _pMsgEID_
  
> [in]オブジェクトのエントリ識別子へのポインター。 
    
 _pszMsgID_
  
> [out]返される ASCII 文字列へのポインター。 _cbStoreRecordKey_ パラメーターが 0 より大きい場合 _、pszMsgID_ パラメーターはテキストに変換された複合エントリ識別子をポイントします。 _cbStoreRecordKey_ が 0 の場合 _、pszMsgID_ はテキストに変換された非コンパイルエントリ識別子をポイントします。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

複合エントリ識別子が作成されるメッセージまたは他のオブジェクトがメッセージ ストアに存在する場合、識別子文字列はオブジェクトのエントリ識別子とストアのレコード キーから作成されます。 オブジェクトがストア内にない場合、つまり  _cbStoreRecordKey_ パラメーターで渡されるストア レコード キーのバイト 数が 0 の場合、オブジェクトのエントリ識別子は単にコピーされ、文字列に変換されます。 
  
**HrComposeMsgID** 関数を呼び出すのは [、HrComposeEID](hrcomposeeid.md)関数を呼び出してから [HrSzFromEntryID](hrszfromentryid.md)関数を呼び出すのと同じです。 
  
 **HrComposeMsgID を** 使用すると、クライアント アプリケーションは複合エントリ識別子を使用して複数のストア内のオブジェクトを操作できます。 アプリケーションは [、HrDecomposeMsgID](hrdecomposemsgid.md) 関数を呼び出して、複合エントリ識別子を元の構成要素に分割できます。 
  

