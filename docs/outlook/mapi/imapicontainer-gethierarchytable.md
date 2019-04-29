---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: efc7f7a2fa703004afe361d766e0209ba40ffe46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426199"
---
# <a name="imapicontainergethierarchytable"></a>IMAPIContainer::GetHierarchyTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナーの階層テーブルへのポインターを返します。
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番テーブルでの情報の返さ方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
CONVENIENT_DEPTH 
  
> 階層テーブルに複数のレベルのコンテナーを格納します。 CONVENIENT_DEPTH が設定されていない場合、階層テーブルにはコンテナーの直下の子コンテナーのみが含まれます。
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable**は、呼び出し元がテーブルを使用できるようになる前に、正常に返すことができます。 テーブルが使用できない場合は、次のテーブル呼び出しを行うとエラーが発生する可能性があります。 
    
MAPI_UNICODE 
  
> 文字列データを含む列を Unicode 形式で返すように要求します。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式で返されます。 
    
SHOW_SOFT_DELETES
  
> 現在、削除済みアイテムの保存期間の段階にあるとマークされているアイテムを表示します。
    
 _lpptable_
  
> 読み上げ階層テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 階層テーブルが正常に取得されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
MAPI_E_NO_SUPPORT 
  
> コンテナーは子コンテナーを持たず、階層テーブルを提供できません。
    
## <a name="remarks"></a>注釈

**IMAPIContainer:: GetHierarchyTable**メソッドは、コンテナーの階層テーブルへのポインターを返します。 階層テーブルは、コンテナー内の子コンテナーに関する概要情報を保持します。 フォルダー階層テーブルは、サブフォルダーに関する情報を保持します。アドレス帳階層テーブルは、子アドレス帳コンテナーおよび配布リストに関する情報を保持します。 
  
一部のコンテナーに子コンテナーを持たせることはできません。 これらのコンテナーは、 **GetHierarchyTable**の実装から MAPI_E_NO_SUPPORT を返します。
  
CONVENIENT_DEPTH フラグが設定されている場合、階層テーブル内の各行には、 **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) プロパティも列として含まれます。 **PR_DEPTH**は、テーブルを実装するコンテナーを基準とした、各コンテナーのレベルを示します。 実装するコンテナーの直下の子コンテナーは、深さ0、深さが0のコンテナー内の子コンテナーは深さ1というようになります。 **PR_DEPTH**の値は、deepens レベルの階層として順番に増加します。 
  
階層テーブルで必須および省略可能な列の完全な一覧については、「 [hierarchy tables](hierarchy-tables.md)」を参照してください。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

コンテナーの階層テーブルをサポートしている場合は、次の操作も実行する必要があります。
  
- コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドの呼び出しをサポートして、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) プロパティを開きます。
    
- コンテナーの[imapiprop:: getproplist](imapiprop-getproplist.md)または[imapiprop:: GetProps](imapiprop-getprops.md)メソッドへの呼び出しから**PR_CONTAINER_HIERARCHY**を返します。 
    
## <a name="notes-to-callers"></a>呼び出し側への注意

文字列およびバイナリコンテンツの表の列を切り捨てられます。 通常、プロバイダーは255文字を返します。 テーブルに切り捨てられた列が含まれているかどうかを事前に知ることはできないため、列の長さが255または510バイトの場合は、列が切り捨てられていると仮定します。 必要に応じて、エントリ id を使用して、切り捨てられた列の完全な値をオブジェクトから直接取得して、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出すことができます。 
  
プロバイダーの実装に応じて、制限および並べ替え操作は、文字列全体またはその文字列の切り捨てられたバージョンに適用できます。 さらに、ストアプロバイダーは、階層テーブルに指定されたソート順序セット[ssortorderset](ssortorderset.md)を優先することは保証されません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl  <br/> |CHierarchyTableTreeCtrl:: GetHierarchyTable  <br/> |CHierarchyTableTreeCtrl クラスは、 **GetHierarchyTable**を使用して、ツリービューコントロールに表示する階層テーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[PidTagContainerHierarchy 標準プロパティ](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

