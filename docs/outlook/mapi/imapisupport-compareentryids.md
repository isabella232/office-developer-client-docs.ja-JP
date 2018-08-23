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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c939189c2c8f7d3147c3146f55deac0e032ce9df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800736"
---
# <a name="imapisupportcompareentryids"></a>IMAPISupport::CompareEntryIDs

  
  
**適用対象**: Outlook 
  
同じオブジェクトを参照しているかどうかを決定する 2 つのエントリ id を比較します。 
  
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
  
> [in]_LpEntryID1_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID1_
  
> [in]比較する最初のエントリの識別子へのポインター。
    
 _cbEntryID2_
  
> [in]_LpEntryID2_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID2_
  
> [in]比較する 2 番目のエントリの識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulResult_
  
> [out]比較の結果へのポインター。 2 つのエントリの識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合、FALSE です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 比較は正常に終了しました。
    
MAPI_E_UNKNOWN_ENTRYID 
  
> いずれかまたは両方のパラメーターとして指定されているエントリの識別子を参照しない有効なオブジェクトは、可能性がありますが現在開かれていないと使用できないためです。
    
## <a name="remarks"></a>注釈

アドレス帳、メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::CompareEntryIDs**メソッドを実装します。 **CompareEntryIDs**は、同じオブジェクトを参照しているかどうかを決定する 1 つのサービス プロバイダーに属している 2 つのエントリ id を比較します。 MAPI では、オブジェクトを担当するサービス ・ プロバイダーを決定するエントリの識別子から[MAPIUID](mapiuid.md)の部分を抽出します。 MAPI は、比較を実行するよう、ログオン オブジェクトの**CompareEntryIDs**メソッドを呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **CompareEntryIDs**は、オブジェクトが 1 つ以上の有効なエントリ id を持つことができますので便利です。 このような状況には、たとえば、サービス ・ プロバイダーの新しいバージョンをインストールした後が発生します。 
  
**CompareEntryIDs**がエラーを返した場合は、比較の結果に基づいてアクションになりません。 代わりにかかる可能性のある最も保守的なアプローチをします。 **CompareEntryIDs**は、エントリの識別子のいずれかで無効な**MAPIUID**構造が含まれているなどの場合に失敗する可能性があります。 
  
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

