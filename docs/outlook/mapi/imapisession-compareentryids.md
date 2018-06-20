---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: df6347298aab5404ec69bd9ac876863e31b741d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800698"
---
# <a name="imapisessioncompareentryids"></a>IMAPISession::CompareEntryIDs

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

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
  
> いずれかまたは両方のパラメーターとして指定されているエントリの識別子を参照しないオブジェクト、可能性のあるこれらのオブジェクトは、現在開かれていないと使用できないためです。
    
## <a name="remarks"></a>備考

**IMAPISession::CompareEntryIDs**メソッドは、同じオブジェクトを参照しているかどうかを決定する 1 つのサービス プロバイダーに属している 2 つのエントリ id を比較します。 MAPI は、オブジェクトを担当するサービス ・ プロバイダーを決定するエントリの識別子から[MAPIUID](mapiuid.md)の部分を抽出し、比較を実行するのには、そのログオン オブジェクトの**CompareEntryIDs**メソッドを呼び出して、します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**CompareEntryIDs**メソッドは、オブジェクトが 1 つ以上の有効なエントリ id を持つことができますので便利です。 このような状況には、たとえば、サービス ・ プロバイダーの新しいバージョンをインストールした後が発生します。 
  
**CompareEntryIDs**がエラーを返した場合は、比較の結果に基づいてアクションになりません。 代わりにかかる可能性のある最も保守的なアプローチをします。 **CompareEntryIDs**は、一方または両方のエントリの識別子で、無効な**MAPIUID**が含まれているなどの場合に失敗する可能性があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CbaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI では、 **IMAPISession::CompareEntryIDs**メソッドを使用して、ユーザーが入力した 2 つのエントリ Id を比較します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

