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
  
> [in]テーブルで情報を返す方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
CONVENIENT_DEPTH 
  
> 階層テーブルに複数のレベルのコンテナーを入力します。 このCONVENIENT_DEPTH設定されていない場合、階層テーブルにはコンテナーの直接の子コンテナーだけが含まれます。
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable は** 、呼び出し元がテーブルを使用できる前に、正常に返すことができます。 テーブルが使用できない場合は、後続のテーブル呼び出しでエラーが発生する可能性があります。 
    
MAPI_UNICODE 
  
> 文字列データを含む列を Unicode 形式で返す要求。 このフラグMAPI_UNICODE設定しない場合は、文字列を ANSI 形式で返す必要があります。 
    
SHOW_SOFT_DELETES
  
> 現在、削除済みアイテムとしてマークされているアイテム、つまり削除済みアイテムの保持時間フェーズにあるアイテムを表示します。
    
 _lppTable_
  
> [out]階層テーブルへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 階層テーブルが正常に取得されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
MAPI_E_NO_SUPPORT 
  
> コンテナーには子コンテナーが含まれていますが、階層テーブルを指定することはできません。
    
## <a name="remarks"></a>注釈

**IMAPIContainer::GetHierarchyTable** メソッドは、コンテナーの階層テーブルへのポインターを返します。 階層テーブルには、コンテナー内の子コンテナーに関する概要情報が格納されます。 フォルダー階層テーブルには、サブフォルダーに関する情報が格納されます。アドレス帳階層テーブルには、子アドレス帳コンテナーと配布リストに関する情報が格納されます。 
  
一部のコンテナーに子コンテナーがない場合があります。 これらのコンテナーは **、getHierarchyTable** MAPI_E_NO_SUPPORT実装からデータを返します。
  
このフラグCONVENIENT_DEPTH設定すると、階層テーブルの各行には、PR_DEPTH **(** [PidTagDepth](pidtagdepth-canonical-property.md)) プロパティも列として含まれます。 **PR_DEPTH** は、テーブルを実装するコンテナーに対する各コンテナーのレベルを示します。 実装するコンテナーの直接の子コンテナーは深度 0、深度 0 のコンテナーの子コンテナーは深度 1 などです。 レベルの階層 **が深PR_DEPTH、** 値は順次増加します。 
  
階層テーブルの必須列とオプション列の完全な一覧については、「階層テーブル」 [を参照してください](hierarchy-tables.md)。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

コンテナーの階層テーブルをサポートする場合は、次の操作も行う必要があります。
  
- コンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドの呼び出しをサポートして **、PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) プロパティを開きます。
    
- コンテナー **PR_CONTAINER_HIERARCHY** [IMAPIProp::GetPropList](imapiprop-getproplist.md) または [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドへの呼び出しから返します。 
    
## <a name="notes-to-callers"></a>呼び出し側への注意

文字列およびバイナリコンテンツテーブルの列は切り捨て可能です。 通常、プロバイダーは 255 文字を返します。 テーブルに切り捨てられた列が含まれるかどうかは事前に分からないので、列の長さが 255 バイトまたは 510 バイトの場合は、列が切り捨てられると仮定します。 必要に応じて、切り捨てられた列の完全な値をオブジェクトから直接取得するには、そのエントリ識別子を使用して開き [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出します。 
  
プロバイダーの実装に応じて、制限と並べ替え操作は、文字列全体またはその文字列の切り捨てられたバージョンに適用できます。 さらに、ストア プロバイダーは、階層テーブルに指定された並べ替え順序セット [SSortOrderSet を](ssortorderset.md) 受け入れ保証されません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |CHierarchyTableTreeCtrl クラスは **GetHierarchyTable** を使用して、ツリー ビュー コントロールに表示する階層テーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[PidTagContainerHierarchy 標準プロパティ](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

