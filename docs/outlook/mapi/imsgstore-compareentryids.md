---
title: IMsgStoreCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 640923511241b08e5a86e9733aab5cc2e9237c23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576576"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ ストアの同じエントリを参照しているかどうかを決定する 2 つのエントリ id を比較します。 MAPI は、両方のエントリの識別子を比較するには、一意の識別子 (Uid) がそのプロバイダーによって処理される場合にのみ、サービス ・ プロバイダーへの呼び出しを渡します。
  
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
  
> [in]_._ _LpEntryID1_パラメーターで指定されたエントリの識別子のバイト数
    
 _lpEntryID1_
  
> [in]比較する最初のエントリの識別子へのポインター。
    
 _cbEntryID2_
  
> [in]_._ _LpEntryID2_パラメーターで指定されたエントリの識別子のバイト数
    
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
  
> 一方または両方のパラメーターを参照しないオブジェクトでは、場合によって対応するオブジェクトが開かれていないとには利用できませんので、指定されたエントリの識別子が表示されます。
    
## <a name="remarks"></a>注釈

**IMsgStore::CompareEntryIDs**メソッドは、同じオブジェクトを参照しているかどうかを確認するメッセージ ・ ストアに属する 2 つのエントリ id を比較します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **CompareEntryIDs**は、オブジェクト (たとえば、メッセージ ストア プロバイダーの新しいバージョンをインストールした後) の 2 つ以上の有効なエントリ id を持つことができますので便利です。 
  
**CompareEntryIDs**がエラーを返した場合は、比較の結果に基づいてアクションになりません。 代わりにかかる可能性のある最も保守的なアプローチをします。 **CompareEntryIDs**は、一方または両方のエントリの識別子で、無効な**MAPIUID**が含まれているなどの場合に失敗する可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI では、 **IMsgStore::CompareEntryIDs**メソッドを使用して、エントリ Id を比較します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

