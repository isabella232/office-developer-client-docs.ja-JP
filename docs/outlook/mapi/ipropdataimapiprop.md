---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d6a53d112e4c12cd9092ac627e99cf3c13d901f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801147"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**適用対象**: Outlook 
  
取得し、オブジェクトのプロパティに対するアクセス権を変更する機能を提供します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって公開されます。  <br/> |データ オブジェクトのプロパティ  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダーとクライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIPropData  <br/> |
|ポインターの型。  <br/> |LPPROPDATA  <br/> |
|トランザクション モデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |�I�u�W�F�N�g�̃A�N�Z�X ���x����ݒ肵�܂��B  <br/> |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |状態の 1 つまたは複数オブジェクトのプロパティのアクセス レベルを設定します。  <br/> |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |�A�N�Z�X ���x���� 1 �܂��͕����̃I�u�W�F�N�g�̃v���p�e�B�̏�Ԃ�擾���܂��B  <br/> |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |PT_OBJECT の種類の 1 つまたは複数のプロパティをオブジェクトに追加します。  <br/> |
   
## <a name="remarks"></a>注釈

**IPropData::IMAPIProp**インターフェイスは、MAPI によって実装され、 [CreateIProp](createiprop.md)関数を呼び出して、この実装にアクセスするサービス プロバイダーによって主に使用されます。 
  
オブジェクトおよびプロパティのアクセス レベルに関する詳細については、[オブジェクトとプロパティのアクセス許可](permissions-for-mapi-objects-and-properties.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

