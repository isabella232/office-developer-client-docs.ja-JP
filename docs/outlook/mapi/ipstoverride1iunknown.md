---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315499"
---
# <a name="ipstoverride1--iunknown"></a>IPSTOVERRIDE1 : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用フォルダーファイル (PST) ストアプロバイダーが PSTDisableGrow ポリシーを上書きできるようにします。
  
|||
|:-----|:-----|
|継承元:  <br/> |IUnknown  <br/> |
|実装元:  <br/> |PST ストアプロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|インターフェイス識別子:  <br/> |IID_IPSTOVERRIDE1  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[IPSTOVERRIDE1::GetPersistedRegistrations](ipstoverride1-getpersistedregistrations.md) <br/> |個人用フォルダー (.pst) ファイルの登録リストを取得します。  <br/> |
|[IPSTOVERRIDE1::SetPersistedRegistrations](ipstoverride1-setpersistedregistrations.md) <br/> |自動的にロックを解除する個人用フォルダーファイルを登録して、HrTrustedPSTOverrideHandlerCallback へのその他の呼び出しを回避します。  <br/> |
|[IPSTOVERRIDE1::OverridePSTDisableGrow](ipstoverride1-overridepstdisablegrow.md) <br/> |拡張のために個人用フォルダーファイルのロックを解除します。  <br/> |
   
## <a name="remarks"></a>解説

現在使用しているダウンロード可能なヘッダーファイルでは、PST オーバーライドハンドラインターフェイス識別子が定義されていない場合があります。その場合は、 [MAPI の定数](mapi-constants.md)のトピックに記載されているので、それをコピーしてコードに追加できます。 Microsoft Windows Software Development Kit (SDK) ヘッダーファイル guiddef で定義されている DEFINE_GUID マクロを使用して、グローバル一意識別子 (GUID) シンボリック名を値に関連付けます。 
  
詳細については、「 [Outlook 2007 で PSTDisableGrow ポリシーをバイパスするように PST オーバーライドハンドラーを実装する方法](https://support.microsoft.com/kb/956070)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

