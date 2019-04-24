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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317270"
---
# <a name="imsprovidercomparestoreids"></a>IMSProvider::CompareStoreIDs

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2つのメッセージストアエントリ識別子を比較して、同じ store オブジェクトを参照しているかどうかを判断します。
  
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
  
> 順番_lpEntryID1_パラメーターによって示されるエントリ識別子のバイト単位のサイズ _。_
    
 _lpEntryID1_
  
> 順番比較する最初のエントリ識別子へのポインター。
    
 _cbEntryID2_
  
> 順番_lpEntryID2_パラメーターによって示されるエントリ識別子のバイト単位のサイズ _。_
    
 _lpEntryID2_
  
> 順番比較する2番目のエントリ id へのポインター。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lルー result_
  
> 読み上げ返された比較結果へのポインター。 2つのエントリ識別子が同じオブジェクトを参照している場合は TRUE。それ以外の場合は FALSE。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

MAPI は、 [imapisession:: openmsgstore](imapisession-openmsgstore.md)メソッドへの呼び出しを処理するときに、 **IMSProvider:: comparestoreids**メソッドを呼び出します。 **comparestoreids**はこの時点で呼び出され、開いているメッセージストアに関連付けられているプロファイルセクションがある場合は、それを判断します。 **comparestoreids**呼び出しは、特定のストアプロバイダーに対してメッセージストアが開かれていない場合に行うことができます。 さらに、MAPI は、 [imapisupport::](imapisupport-openprofilesection.md) openprofileupdatemethod へのストアプロバイダー呼び出しを処理するときに、 **comparestoreids**も呼び出します。 
  
**comparestoreids**によって比較されるエントリ識別子は、現在のストアプロバイダーのダイナミックリンクライブラリ (DLL) と共に、かつ非ラップストアエントリ識別子の両方になります。 ストアエントリ識別子のラッピングの詳細については、「 [imapisupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md)」を参照してください。
  
エントリ識別子の比較は、1つのオブジェクトが複数の有効なエントリ識別子を持つことができるので便利です。 これは、たとえば、新しいバージョンのメッセージストアプロバイダーがインストールされた後に発生する可能性があります。 
  
## <a name="see-also"></a>関連項目



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

