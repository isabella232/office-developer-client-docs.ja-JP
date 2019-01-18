---
title: キーセット カーソル (デスクトップ データベース参照のアクセス)
TOCTitle: Keyset cursors
ms:assetid: 4b6e5f90-4413-4fb3-0a08-2cb89d3c61f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249236(v=office.15)
ms:contentKeyID: 48544690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 200b10599683a5b5877952664c04e94b2523cfee
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721921"
---
# <a name="keyset-cursors"></a><span data-ttu-id="cf79c-102">キーセット カーソル</span><span class="sxs-lookup"><span data-stu-id="cf79c-102">Keyset cursors</span></span>

<span data-ttu-id="cf79c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cf79c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cf79c-p101">キーセット カーソルの変更検出機能は、静的カーソルと動的カーソルの中間です。静的カーソルと同様、キーセット カーソルでは、結果セットのメンバーシップと順序に対する変更が常に検出されるわけではありません。一方、結果セット内の行の値に対する変更は、動的カーソルと同様に検出されます。</span><span class="sxs-lookup"><span data-stu-id="cf79c-p101">The keyset cursor provides functionality between a static and a dynamic cursor in its ability to detect changes. Like a static cursor, it does not always detect changes to the membership and order of the result set. Like a dynamic cursor, it does detect changes to the values of rows in the result set.</span></span>

<span data-ttu-id="cf79c-p102">キーセット ドリブン カーソルは、キーセットと呼ばれる一意の識別子 (キー) のセットによって制御されます。キーは、結果セット内の行を一意に識別する列のセットで構成されます。キーセットは、クエリ ステートメントによって返されたすべての行のキー値のセットです。</span><span class="sxs-lookup"><span data-stu-id="cf79c-p102">Keyset-driven cursors are controlled by a set of unique identifiers (keys) known as the keyset. The keys are built from a set of columns that uniquely identify the rows in the result set. The keyset is the set of key values from all the rows returned by the query statement.</span></span>

<span data-ttu-id="cf79c-p103">キーセット ドリブン カーソルを使用すると、行ごとにキーが作成されてカーソル内に保存され、クライアント ワークステーション、またはサーバー上に格納されます。各行にアクセスすると、格納されたキーを使用してデータ ソースから現在のデータがフェッチされます。キーセット ドリブン カーソルでは、キーセットがすべて読み込まれた時点で、結果セットのメンバーシップが凍結されます。それ以降にメンバーシップに影響する追加や更新が行われても、結果セットを再度開かない限り、結果セットには反映されません。</span><span class="sxs-lookup"><span data-stu-id="cf79c-p103">With keyset-driven cursors, a key is built and saved for each row in the cursor and stored either on the client workstation or on the server. When you access each row, the stored key is used to fetch the current data values from the data source. In a keyset-driven cursor, result set membership is frozen when the keyset is fully populated. Thereafter, additions or updates that affect membership are not a part of the result set until it is reopened.</span></span>

<span data-ttu-id="cf79c-p104">キーセットの所有者または他のプロセスによってデータ値が変更されると、ユーザーが結果セット内をスクロールすると同時に、その変更が反映されます。カーソルの外側で (他のプロセスによって) 行われた挿入は、カーソルが閉じられ、再度開かれたときに初めて反映されます。カーソル内で行われた挿入は、結果セットの末尾に追加されます。</span><span class="sxs-lookup"><span data-stu-id="cf79c-p104">Changes to data values (made either by the keyset owner or other processes) are visible as the user scrolls through the result set. Inserts made outside the cursor (by other processes) are visible only if the cursor is closed and reopened. Inserts made from inside the cursor are visible at the end of the result set.</span></span>

<span data-ttu-id="cf79c-p105">キーセット ドリブン カーソルが、削除された行を取得しようとすると、その行は結果セット内で "穴" として表されます。その行のキーはキーセット内に存在しますが、行は結果セット内に存在しません。行内のキー値が更新された場合、その行はいったん削除されてから挿入されたと見なされるため、これも結果セット内で穴として表されます。キーセット ドリブン カーソルは、他のプロセスによって削除された行を必ず検出できますが、自身が削除した行のキーを削除するかどうかはオプションです。キーセット ドリブン カーソルでこの処理を行う場合、行が存在した証拠が消失してしまうため、カーソルは自身が行った削除を検出できません。</span><span class="sxs-lookup"><span data-stu-id="cf79c-p105">When a keyset-driven cursor attempts to retrieve a row that has been deleted, the row appears as a "hole" in the result set. The key for the row exists in the keyset, but the row no longer exists in the result set. If the key values in a row are updated, the row is considered to have been deleted and then inserted, so such rows also appear as holes in the result set. While a keyset-driven cursor can always detect rows deleted by other processes, it can optionally remove the keys for rows it deletes itself. Keyset-driven cursors that do this cannot detect their own deletes because the evidence has been removed.</span></span>

<span data-ttu-id="cf79c-p106">キー列を更新すると、前のキーを削除してから新しいキーを挿入した場合と同様の処理が行われます。更新がカーソルを通じて実行されない限り、新しいキーは反映されません。更新がカーソルを通じて実行された場合、新しいキーは結果セットの末尾に追加されます。</span><span class="sxs-lookup"><span data-stu-id="cf79c-p106">An update to a key column operates like a delete of the old key followed by an insert of the new key. The new key value is not visible if the update was not made through the cursor. If the update was made through the cursor, the new key value is visible at the end of the result set.</span></span>

<span data-ttu-id="cf79c-p107">キーセット ドリブン カーソルの一種として、キーセット ドリブン標準カーソルと呼ばれるものがあります。キーセット ドリブン標準カーソルでは、結果セット内の行のメンバーシップ、および行の順序が、カーソルが開かれたときの状態で固定されますが、カーソルの所有者が値を変更した場合や、他のプロセスによって行われた変更がコミットされた場合は、その変更が反映されます。変更によって、行がメンバーシップの条件に適合しなくなったり、行の順序が変化したりしても、カーソルが閉じられて再度開かれない限り、その行が削除または移動されることはありません。挿入されたデータは反映されませんが、既存のデータに対する変更は、行のフェッチと同時に反映されます。</span><span class="sxs-lookup"><span data-stu-id="cf79c-p107">There is a variation on keyset-driven cursors called keyset-driven standard cursors. In a keyset-driven standard cursor, the membership of rows in the result set and the order of the rows are fixed at cursor open time, but changes to values that are made by the cursor owner and committed changes made by other processes are visible. If a change disqualifies a row for membership or affects the order of a row, the row does not disappear or move unless the cursor is closed and reopened. Inserted data does not appear, but changes to existing data do appear as the rows are fetched.</span></span>

<span data-ttu-id="cf79c-p108">これまで述べてきたように、データの変更による影響は多くのさまざまな状況によって左右されるため、キーセット ドリブン カーソルを正しく使用するには注意が必要です。しかし、アプリケーションにおいて同時更新による影響が少なく、誤ったキーをプログラム上で処理でき、キーで指定された特定の行に直接アクセスする必要がある場合は、キーセット ドリブン カーソルが最適です。ADO でキーセット カーソルを使用することを示すには、 **adOpenKeyset** **CursorTypeEnum** を使用します。</span><span class="sxs-lookup"><span data-stu-id="cf79c-p108">The keyset-driven cursor is difficult to use correctly because the sensitivity to data changes depends on many differing circumstances, as described above. However, if your application is not concerned with concurrent updates, can programmatically handle bad keys, and must directly access certain keyed rows, the keyset-driven cursor might work for you. Use the **adOpenKeyset** **CursorTypeEnum** to indicate that you want to use a keyset cursor in ADO.</span></span>

