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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418107"
---
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
microsoft exchange server table オブジェクトへのアクセスをサポートします。特に、システムアクセス制御リスト (SACL) テーブルオブジェクトと、microsoft exchange server フォルダー上のルールテーブルオブジェクトへのアクセスをサポートします。 このインターフェイスは、 [IMAPITable: IUnknown](imapitableiunknown.md)インターフェイスに似ていますが、sacl とルールを制御するために使用される Microsoft Exchange Server 固有の構造のサポートが追加されています。 
  
|||
|:-----|:-----|
|公開者:  <br/> |なし  <br/> |
|実装元:  <br/> |サーバーテーブルオブジェクト  <br/> |
|呼び出し元:  <br/> |MAPI およびクライアントアプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IExchangeModifyTable  <br/> |
|ポインターの種類:  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|トランザクションモデル:  <br/> |一括  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](iexchangemodifytable-getlasterror.md) <br/> |table オブジェクトで発生した最後のエラーについての情報を返します。  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |MAPI table オブジェクトのインターフェイスへのポインターを返します。  <br/> |
|[modifytable](iexchangemodifytable-modifytable.md) <br/> |MAPI テーブルオブジェクトを更新します。  <br/> |
   
|**ルールテーブルを変更するために使用されるプロパティ**|**Access**|
|:-----|:-----|
|**PR_RULE_ACTIONS**([PidTagRuleActions](pidtagruleactions-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_CONDITION**([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_ID**([PidTagRuleId](pidtagruleid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_LEVEL**([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_NAME**([PidTagRuleName](pidtagrulename-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_PROVIDER**([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_PROVIDER_DATA**([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_SEQUENCE**([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_STATE**([PidTagRuleState](pidtagrulestate-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RULE_USER_FLAGS**([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
|**SACL テーブルを変更するために使用されるプロパティ**|**Access**|
|:-----|:-----|
|**PR_MEMBER_ENTRYID**([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MEMBER_ID**([PidTagMemberId](pidtagmemberid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MEMBER_NAME**([PidTagMemberName](pidtagmembername-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MEMBER_RIGHTS**([PidTagMemberRights](pidtagmemberrights-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

**IExchangeModifyTable**インターフェイスを取得するには、folder オブジェクトの PT_OBJECT 型のプロパティに対して MAPI [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出します。 **openproperty**メソッドを呼び出すときに、 _lpiid_パラメーターの値**IID_IExchangeModifyTable**を渡します。 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

