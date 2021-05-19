---
title: IMAPIFormInfo IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417365"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションに、フォーム定義に特定のプロパティへのアクセス権を与えます。 フォーム情報を別のオブジェクトに保持することで、フォーム ライブラリ プロバイダーは、フォームをアクティブ化せずに、クライアントにフォームを記述できます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|次のユーザーによって公開されます。  <br/> |フォーム情報オブジェクト  <br/> |
|実装元:  <br/> |フォーム ライブラリ プロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIFormInfo  <br/> |
|ポインターの種類:  <br/> |LPMAPIFORMINFO  <br/> |
|トランザクション モデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |フォームで使用されるプロパティの完全なセットへのポインターを返します。  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |フォームで使用される動詞の完全なセットへのポインターを返します。  <br/> |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |フォームのアイコン プロパティからアイコンを作成します。  <br/> |
|[SaveForm](imapiforminfo-saveform.md) <br/> |特定のフォームの説明を構成ファイルに保存します。  <br/> |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |特定のフォームがインストールされているフォーム コンテナーへのポインターを返します。  <br/> |
   
## <a name="remarks"></a>注釈

MapiForm.h ヘッダー ファイルで定義されているほとんどのインターフェイスとは異なり **、IMAPIFormInfo は IMAPIProp** インターフェイスから継承します。ほとんどのフォーム情報は [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドへの呼び出しによってエクスポートされます。 [](imapipropiunknown.md) 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

