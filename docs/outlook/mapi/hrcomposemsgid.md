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
  
オブジェクトの複合エントリ識別子 (通常はメッセージストア内のメッセージ) を表す ASCII 文字列を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
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
  
> 順番クライアントアプリケーションによって使用されているセッションへのポインター。 
    
 _cbStoreRecordKey_
  
> 順番メッセージまたはその他のオブジェクトを含むメッセージストアのレコードキーのサイズ (バイト単位)。 _cbStoreRecordKey_パラメーターに0が渡された場合、 _pszMsgID_パラメーターは、テキストに変換されたエントリ id のコピーを指します。 
    
 _pStoreRecordKey_
  
> 順番メッセージまたはその他のオブジェクトを含むメッセージストアの record キーへのポインター。 
    
 _cbmsgeid_
  
> 順番メッセージまたはその他のオブジェクトのエントリ識別子のサイズ (バイト単位)。 
    
 _pmsgeid_
  
> 順番オブジェクトのエントリ識別子へのポインター。 
    
 _pszMsgID_
  
> 読み上げ返された ASCII 文字列へのポインター。 _cbStoreRecordKey_パラメーターが0より大きい場合、 _pszMsgID_パラメーターは、テキストに変換された複合エントリ識別子を指します。 _cbStoreRecordKey_が0の場合、 _pszMsgID_は、テキストに変換された非複合エントリ識別子を指します。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

複合エントリ識別子が作成されているメッセージまたはその他のオブジェクトがメッセージストアに存在する場合、識別子文字列は、オブジェクトのエントリ識別子とストアの record キーから作成されます。 オブジェクトがストアに存在しない場合、つまり、 _cbStoreRecordKey_パラメーターで渡されたストアレコードキーのバイト数が0の場合、オブジェクトのエントリ識別子は単にコピーされ、文字列に変換されます。 
  
**HrComposeMsgID**関数の呼び出しは、hr の[id](hrcomposeeid.md)関数を呼び出し、次に[hrszfromentryid](hrszfromentryid.md)関数を呼び出すことと同じです。 
  
 **HrComposeMsgID**では、クライアントアプリケーションが複合エントリ識別子を使用して、複数のストア内のオブジェクトを操作することができます。 アプリケーションは[HrDecomposeMsgID](hrdecomposemsgid.md)関数を呼び出して、複合エントリ識別子を元の constituents に分割できます。 
  

