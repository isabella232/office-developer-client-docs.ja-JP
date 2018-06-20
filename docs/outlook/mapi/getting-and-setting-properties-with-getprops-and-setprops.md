---
title: GetProps と SetProps プロパティの設定を取得および
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5751dc8b06d40b9f07a39f05868c328d64c27762
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800176"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>GetProps と SetProps プロパティの設定を取得および
 
**適用されます**: Outlook 
  
、可能な限りしようとするを取得または[IMAPIProp::GetProps](imapiprop-getprops.md)および[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを使用してプロパティを変更します。 プロパティを使用しているが非常に大きい場合を除き、これらのメソッドが適切な場合があります。 その他の場合は読み取りまたは[IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)インターフェイスを使用してストリームに書き込みします。 ストリームでは、非常に大規模なプロパティを正常に処理できますが、リソースを大きく消費 COM ライブラリが必要なためです。 **IMAPIProp::GetProps**または**IMAPIProp::SetProps**呼び出しが失敗した後にのみ、 **IStream**インターフェイスを使用します。 
  

