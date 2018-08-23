---
title: IMSProviderCompareStoreIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.CompareStoreIDs
api_type:
- COM
ms.assetid: c3e3cfaa-9c4a-482a-9411-9c4ab01d312f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 57b8438d655b3bc5b708fd7ed6734554a3a23ac4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585991"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
比較 2 つのメッセージが同じストア オブジェクトを参照しているかどうかを判断するのには、ストア エントリ id です。
  
```cpp
HRESULT CompareStoreIDs(
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
  
> [in]_._ _LpEntryID1_パラメーターで指定されたエントリの識別子のバイト単位のサイズ
    
 _lpEntryID1_
  
> [in]比較する最初のエントリの識別子へのポインター。
    
 _cbEntryID2_
  
> [in]_._ _LpEntryID2_パラメーターで指定されたエントリの識別子のバイト単位のサイズ
    
 _lpEntryID2_
  
> [in]比較する 2 番目のエントリの識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulResult_
  
> [out]比較の結果が返されましたへのポインター。 2 つのエントリの識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合、FALSE です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

MAPI は、 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)メソッドの呼び出しを処理するときに、 **IMSProvider::CompareStoreIDs**メソッドを呼び出します。 **CompareStoreIDs**は、どのプロファイルのセクションでは、存在する場合に関連付けられています開かれているメッセージ ・ ストアを決定するこの時点で呼び出されます。 特定のストア プロバイダーの開いているメッセージ ・ ストアがない場合、 **CompareStoreIDs**の呼び出しを作成できます。 さらに、MAPI ではまた**CompareStoreIDs**を呼び出しして、ストア プロバイダーの[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッド呼び出しを処理するとき。 
  
エントリ id が**CompareStoreIDs**の比較には、プロバイダーのダイナミック リンク ライブラリ (DLL) を格納し、両方のラップ解除済みストア エントリ id は、現在の両方です。 ストア エントリ id の折り返しの詳細については、 [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)を参照してください。
  
エントリ id を比較することは、オブジェクトが 1 つ以上の有効なエントリ id を持つことができますので便利です。 これは、たとえば、メッセージ ストア プロバイダーの新しいバージョンをインストールした後に発生します。 
  
## <a name="see-also"></a>関連項目



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

