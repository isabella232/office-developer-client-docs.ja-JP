---
title: IExchangeModifyTable IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable
api_type:
- COM
ms.assetid: 45a73c7b-5855-4b70-866b-facb41cb3c32
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1093975e6cbdd79004125a0a4a3098ffa421ab0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800431"
---
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable: IUnknown

  
  
**適用されます**: Outlook 
  
Microsoft Exchange Server のテーブルのオブジェクトへのアクセスをサポートしています、具体的にはシステムへのアクセス制御リスト (SACL) テーブルのオブジェクトと、Microsoft Exchange Server フォルダーで table オブジェクトを除外します。 このインターフェイスのような[IMAPITable: IUnknown](imapitableiunknown.md)インタ フェースが、Sacl と規則を制御するために使用されている Microsoft Exchange Server に固有の構造体のサポートの追加。 
  
|||
|:-----|:-----|
|によって公開されます。  <br/> |なし  <br/> |
|によって実装されます。  <br/> |サーバー テーブル オブジェクト  <br/> |
|によって呼び出されます。  <br/> |MAPI クライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IExchangeModifyTable  <br/> |
|ポインターの型。  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|トランザクション モデル:  <br/> |トランザクション処理  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[発生しました](iexchangemodifytable-getlasterror.md) <br/> |Table オブジェクトには、最後に発生したエラーに関する情報を返します。  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |MAPI テーブルのオブジェクトのインターフェイスへのポインターを返します。  <br/> |
|[ModifyTable](iexchangemodifytable-modifytable.md) <br/> |MAPI テーブルのオブジェクトを更新します。  <br/> |
   
|**規則テーブルを変更するためのプロパティ**|**Access**|
|:-----|:-----|
|**PR_RULE_ACTIONS**([PidTagRuleActions](pidtagruleactions-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_RULE_CONDITION**([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_RULE_ID**([PidTagRuleId](pidtagruleid-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_RULE_LEVEL**([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_RULE_NAME**([PidTagRuleName](pidtagrulename-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_RULE_PROVIDER**([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_RULE_PROVIDER_DATA**([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_RULE_SEQUENCE**([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_RULE_STATE**([PidTagRuleState](pidtagrulestate-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_RULE_USER_FLAGS**([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
   
|**SACL のテーブルを変更するためのプロパティ**|**Access**|
|:-----|:-----|
|**PR_MEMBER_ENTRYID**([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_MEMBER_ID**([PidTagMemberId](pidtagmemberid-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_MEMBER_NAME**([PidTagMemberName](pidtagmembername-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_MEMBER_RIGHTS**([PidTagMemberRights](pidtagmemberrights-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
   
## <a name="remarks"></a>備考

**IExchangeModifyTable**インターフェイスを取得するには、PT_OBJECT フォルダー オブジェクトの種類のプロパティに対して MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。 **OpenProperty**メソッドを呼び出すときは、 **IID_IExchangeModifyTable** 、 _lpiid_パラメーターの値を渡します。 
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

