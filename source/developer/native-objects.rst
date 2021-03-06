===================
From Bukkit Objects
===================

Players
=======

Due to legacy reasons, WorldGuard uses its own internal player object called ``LocalPlayer``. A Bukkit ``Player`` can be converted to a ``LocalPlayer`` using ``wrapPlayer(Player)`` on ``WorldGuardPlugin``.

.. code-block:: java

    getWorldGuard().wrapPlayer(player);

Vectors
=======

Many operations need WorldEdit vectors, worlds, and so on. Bukkit ``Locations`` and other objects can be converted to ``Vectors`` using methods in ``com.sk89q.worldedit.bukkit.BukkitAdapter``.

.. code-block:: java

    BukkitAdapter.adapt(location);
    BukkitAdapter.adapt(world);
