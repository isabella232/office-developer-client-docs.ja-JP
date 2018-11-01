---
title: Recordset2.Updatable プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: ad8184b6-ffe3-dde6-ddee-4b23cdaa9c59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821726(v=office.15)
ms:contentKeyID: 48547041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba986d76126b6e805b8bf7a52299cfc16f5841d8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881637"
---
# <a name="recordset2updatable-property-dao"></a>Recordset2.Updatable プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( **Boolean**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。更新可能です

*式***Recordset2**オブジェクトを表す変数です。

## <a name="remarks"></a>備考

スナップショットと前方スクロールのタイプの Recordset オブジェクトは常に**False**を返します。

オブジェクトの種類の中には、更新できないフィールドが含まれている場合がよくあります。たとえば、一部のフィールドしか変更できないようなダイナセット タイプの **Recordset** オブジェクトを作成することもできます。これらのフィールドは固定にすることも、自動的に増加するデータを含めることもでき、また更新可能なテーブルと更新できないテーブルを組み合わせたクエリによってダイナセットを得ることもできます。

オブジェクトに読み取り専用フィールドしか含まれていない場合、 **Updatable** プロパティの値は **False** となります。1 つ以上のフィールドが更新可能な場合、このプロパティの値は **True** となります。更新可能なフィールドのみ編集できます。新しい値を読み取り専用フィールドに割り当てると、トラップ可能なエラーが発生します。

更新可能なオブジェクトには読み取り専用フィールドが含まれていることがあるため、レコードを編集する前に、 **Recordset** オブジェクトの **Fields** コレクションの各フィールドの **DataUpdatable** プロパティを確認する必要があります。

