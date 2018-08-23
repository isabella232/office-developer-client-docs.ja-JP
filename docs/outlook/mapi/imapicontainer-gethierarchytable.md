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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 88b6f220f812f419b3f881aaa7f70a22186b589e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563801"
---
# <a name="imapicontainergethierarchytable"></a>IMAPIContainer::GetHierarchyTable

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
コンテナーの階層構造のテーブルへのポインターを返します。
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]テーブルの情報を返す方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
CONVENIENT_DEPTH 
  
> コンテナーが複数のレベルから階層テーブルに格納します。 CONVENIENT_DEPTH が設定されていない場合、階層テーブルには、コンテナーの直下の子のコンテナーだけが含まれています。
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable**が正常に完了可能性があります前にテーブルが使用可能な呼び出し元にします。 テーブルが使用できない場合は、テーブルのそれ以降の呼び出しを行うとエラーが発生します。 
    
MAPI_UNICODE 
  
> Unicode 形式で文字列データを含む列が返されるように要求します。 MAPI_UNICODE フラグが設定されていない場合、文字列が ANSI 形式で返されます。 
    
SHOW_SOFT_DELETES
  
> ソフトとしてマークされているアイテムの削除を示しています-は削除済みアイテムの保存に時間の段階です。
    
 _lppTable_
  
> [out]階層テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 階層テーブルが正常に取得しました。
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
MAPI_E_NO_SUPPORT 
  
> コンテナーは、子コンテナーがないと、階層テーブルを提供することはできません。
    
## <a name="remarks"></a>注釈

**IMAPIContainer::GetHierarchyTable**メソッドは、コンテナーの階層テーブルにポインターを返します。 階層テーブルは、コンテナー内の子コンテナーに関する要約情報を保持します。 フォルダーの階層テーブルには、サブフォルダーの情報を保持します。アドレス帳階層テーブルは、アドレス帳コンテナーや配布リストに子に関する情報を保持します。 
  
いくつかのコンテナーに子コンテナーがないことができます。 これらのコンテナーでは、 **GetHierarchyTable**の実装から MAPI_E_NO_SUPPORT を返します。
  
CONVENIENT_DEPTH フラグを設定すると、階層テーブル内の各行にはにより、その列としても**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) のプロパティが含まれます。 **PR_DEPTH**は、テーブルを実装するコンテナーを基準にして、各コンテナーのレベルを示します。 深さが 1 というように実装するコンテナーの直下の子コンテナーは、0、0 の深さのコンテナー内の子コンテナーの深さがあります。 レベルの階層を深めるよう、 **PR_DEPTH**の値は順番に増加します。 
  
階層テーブル内の必須および省略可能な列の一覧については、[階層テーブル](hierarchy-tables.md)を参照してください。
  
## <a name="notes-to-implementers"></a>実装者へのメモ

コンテナーの階層テーブルをサポートする場合も、次の行う必要があります。
  
- **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) のプロパティを開くには、コンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出しをサポートしてください。
    
- コンテナーの[IMAPIProp::GetPropList](imapiprop-getproplist.md)または[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドの呼び出しから**PR_CONTAINER_HIERARCHY**を返します。 
    
## <a name="notes-to-callers"></a>呼び出し側への注意

文字列とバイナリの内容のテーブルの列を切り捨てることができます。 通常、プロバイダーは、255 文字を返します。 テーブルには、切り捨てられた列が含まれて かどうか、あらかじめ知ることはできません、ため、列の長さが 255 であるか、510 バイトである場合、列が切り捨てられることを想定しています。 常にから取得できます、切り捨てられた列の最大の価値に応じて、直接オブジェクトを開くには、そのエントリの識別子を使用して、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すことによって。 
  
プロバイダーの実装の制限や並べ替え操作によっては、全体の文字列とその文字列の切り捨てられたバージョンを適用できます。 さらに、ストア プロバイダーは、階層テーブルの[SSortOrderSet](ssortorderset.md)が指定されている並べ替え順序のセットを優先するとは限りません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |CHierarchyTableTreeCtrl クラスでは、 **GetHierarchyTable**を使用して、ツリー ビュー コントロールに表示する階層テーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[PidTagContainerHierarchy 標準プロパティ](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

