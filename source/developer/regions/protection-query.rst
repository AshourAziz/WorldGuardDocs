===================
Querying Protection
===================

To query protection, the ``DefaultFlag.BUILD`` flag can be tested using the methods explained in :doc:`flag-calculation`.

.. tip::
    You can also use the shortcut methods as explained in :doc:`../build-checks`.

.. topic:: Example: Querying build permission using the query cache

    .. code-block:: java

        LocalPlayer localPlayer = getWorldGuard().wrapPlayer(player)
        Location loc = new Location(world, 10, 64, 100);
        RegionContainer container = getWorldGuard().getRegionContainer();
        RegionQuery query = container.createQuery();

        if (!query.testState(loc, localPlayer, DefaultFlag.BUILD)) {
            // Can't build
        }