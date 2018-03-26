## Show creation date of domain registration

    whois slashdot.org | awk '/Creation Date/{print $NF}'