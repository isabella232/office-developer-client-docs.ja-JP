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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 734e53c1e897c902c72319aa6f2d3d7af2d23fb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431709"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2 つのメッセージ ストア エントリ識別子を比較して、同じストア オブジェクトを参照するかどうかを判断します。
  
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
  
> [in]  _lpEntryID1_ パラメーターが指すエントリ識別子のサイズ (バイト  _単位)。_
    
 _lpEntryID1_
  
> [in]比較する最初のエントリ識別子へのポインター。
    
 _cbEntryID2_
  
> [in]  _lpEntryID2_ パラメーターが指すエントリ識別子のサイズ (バイト  _単位)。_
    
 _lpEntryID2_
  
> [in]比較する 2 番目のエントリ識別子へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lpulResult_
  
> [out]比較の返される結果へのポインター。 2 つのエントリ識別子が同じオブジェクトを参照する場合は TRUE。それ以外の場合は FALSE。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

MAPI は [、IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)メソッドへの呼び出しを処理するときに **、IMSProvider::CompareStoreIDs** メソッドを呼び出します。 **この時点で CompareStoreIDs** が呼び出され、開いているメッセージ ストアに関連付けられているプロファイル セクション (ある場合) が特定されます。 **CompareStoreIDs 呼** び出しは、特定のストア プロバイダーに対して開いているメッセージ ストアがない場合に行います。 さらに、MAPI は[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッドへのストア プロバイダー呼び出しを処理するときに CompareStoreIDs も呼び出します。  
  
**CompareStoreIDs** で比較されるエントリ識別子は、現在のストア プロバイダーのダイナミック リンク ライブラリ (DLL) の両方のエントリ識別子であり、両方ともラップされていないストア エントリ識別子です。 ストア エントリ識別子の折り返しの詳細については [、「IMAPISupport::WrapStoreEntryID」を参照してください](imapisupport-wrapstoreentryid.md)。
  
エントリ識別子の比較は、オブジェクトが複数の有効なエントリ識別子を持つ可能性がある場合に便利です。 これは、たとえば、メッセージ ストア プロバイダーの新しいバージョンがインストールされた後に発生する可能性があります。 
  
## <a name="see-also"></a>関連項目



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

