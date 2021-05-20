---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6c79943792c8c17ee007c39b5c5c215a6fbc0699
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431044"
---
# <a name="imapisupportcompareentryids"></a>IMAPISupport::CompareEntryIDs

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID1_
  
> [in]  _lpEntryID1_ パラメーターが指すエントリ識別子のバイト 数。 
    
 _lpEntryID1_
  
> [in]比較する最初のエントリ識別子へのポインター。
    
 _cbEntryID2_
  
> [in]  _lpEntryID2_ パラメーターが指すエントリ識別子のバイト 数。 
    
 _lpEntryID2_
  
> [in]比較する 2 番目のエントリ識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulResult_
  
> [out]比較の結果へのポインター。 2 つのエントリ識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合は FALSE。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 比較は成功しました。
    
MAPI_E_UNKNOWN_ENTRYID 
  
> パラメーターとして指定されたエントリ識別子の 1 つまたは両方は、有効なオブジェクトを参照しません。これは、現在開かないので、使用できない可能性があります。
    
## <a name="remarks"></a>注釈

**IMAPISupport::CompareEntryIDs** メソッドは、アドレス帳およびメッセージ ストア プロバイダーのサポート オブジェクトに実装されます。 **CompareEntryIDs は** 、1 つのサービス プロバイダーに属する 2 つのエントリ識別子を比較して、同じオブジェクトを参照するかどうかを判断します。 MAPI は [、MAPIUID](mapiuid.md) 部分をエントリ識別子から抽出して、オブジェクトを担当するサービス プロバイダーを決定します。 MAPI は、そのログオン オブジェクトの **CompareEntryIDs** メソッドを呼び出して比較を実行します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **CompareEntryIDs は** 、オブジェクトが複数の有効なエントリ識別子を持つ可能性がある場合に便利です。 この状況は、たとえば、サービス プロバイダーの新しいバージョンがインストールされた後に発生する可能性があります。 
  
**CompareEntryIDs が** エラーを返す場合は、比較の結果に基づいてアクションを実行しない。 代わりに、可能な限り最も保守的なアプローチを取ってください。 たとえば、エントリ識別子の一方または両方に無効な MAPIUID 構造が含まれている場合 **、CompareEntryIDs** は **失敗する可能性** があります。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

