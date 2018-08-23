---
title: 構成のプロパティ シートを表示します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fa48e97ed25fe1175ffd3a92ac961dcf5bde50b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588357"
---
# <a name="displaying-configuration-property-sheets"></a>構成のプロパティ シートを表示します。

**適用されます**: Outlook 2013 |Outlook 2016 
  
トランスポート プロバイダーは、プロパティ シートの構成を実装するために[IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)メソッドを使用します。 **DoConfigPropSheet**を呼び出すと、トランスポート プロバイダーはそれらを表示する方法についての情報とプロパティの配列をポインターで渡します。 MAPI ではユーザーにプロパティが、標準のダイアログ ボックスを使用してに表示されます。 一貫性のあるインターフェイスのユーザーにとってのメリットのためのトランスポート プロバイダーを実装する場合、このプロパティ シートのメカニズムを使用するよう強くお勧めします。
  
## <a name="transport-providers"></a>トランスポート プロバイダー

トランスポート プロバイダーは、 **DoConfigPropSheet**で使用するため、表示された表の作成を簡略化するのに[BuildDisplayTable](builddisplaytable.md)関数を使用することができます。 トランスポート プロバイダーは、プロパティ シート API を直接使用することができますもします。 バッファーのプロパティを変更するには、トランスポート プロバイダーは、 [CreateIProp](createiprop.md)関数を使用できます。 ユーザー プロパティに格納されている値を変更するときに、ユーザーがキャンセルの処理が簡素化されます。 かどうか、必要に応じてトランスポート プロバイダーも提供できますウィザード ダイアログ ボックスがユーザーの構成作業を簡略化します。 
  

